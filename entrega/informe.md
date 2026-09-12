# 📄 Informe Técnico del Taller

## 🔖 Nombre del Taller
Taller 5 - Evaluación de Seguridad con STRIDE aplicado a Insuclínicos Ltda.

## 👥 Integrantes del equipo
* espacio jorge (gevengood)
* David Santiago Buendia Londoño (Santiagoob7)

## 🧠 Descripción general del trabajo
El objetivo de este taller fue aplicar el marco de modelado de amenazas STRIDE para evaluar la seguridad de la arquitectura actual (AS-IS) de Insuclínicos Ltda. El análisis se centró en el macro-proceso crítico de **Gestión y Cumplimiento de Pedido**, específicamente en el ecosistema de control operativo basado en archivos locales de Microsoft Excel y la comunicación mediante WhatsApp. A través de este ejercicio, se identificaron vulnerabilidades estructurales en el manejo de la información y se propusieron mitigaciones técnicas viables acordes a las restricciones presupuestales y operativas del cliente.

## 🔧 Proceso de desarrollo
El trabajo se desarrolló siguiendo una metodología estructurada en 5 pasos:
1. **Selección y delimitación:** A partir de los modelos previos (BPMN y ArchiMate AS-IS), acotamos el análisis al PC de Administración, que actúa como el núcleo de datos (pedidos e inventario).
2. **Construcción del DFD:** Dibujamos el diagrama de flujo de datos estableciendo un límite de confianza claro alrededor de la red local y el disco duro donde residen los archivos críticos.
3. **Reconocimiento Pasivo:** En lugar de lanzar ataques, analizamos la topología AS-IS documentada (uso de hardware físico sin redundancia, carpetas compartidas, sesiones locales).
4. **Aplicación de STRIDE:** Redactamos 6 escenarios de amenaza específicos (Suplantación, Alteración, Repudio, Divulgación, Denegación de Servicio y Elevación de Privilegios) adaptados a un entorno de ofimática local, alejándonos de los ejemplos web tradicionales.
5. **Priorización:** Clasificamos los riesgos, destacando como críticos la Denegación de Servicio (punto único de falla del disco duro) y la Alteración (falta de integridad en los Excel).

## 🧩 Análisis del modelo propuesto
El modelo de amenazas entregado refleja de manera precisa la realidad operativa de la PyME. Se estructuró bajo el supuesto de que Insuclínicos no cuenta actualmente con infraestructura en la nube, Active Directory, ni políticas formales de ciberseguridad. 
Las necesidades del cliente frente a la trazabilidad de inventario chocan directamente con los riesgos de **Alteración (Tampering)** y **Repudio (Repudiation)** detectados: al depender de celdas no protegidas y sin historial de versiones, cualquier error humano corrompe la operación. Las mitigaciones propuestas (GPOs, RBAC en NTFS, respaldos 3-2-1 y protección nativa de Office) fueron seleccionadas estratégicamente para mejorar la postura de seguridad sin requerir inversiones inmediatas en licencias de software empresarial.

## 📈 Diagrama final entregado

```mermaid
flowchart TD
    A[Ventas / Administración] -->|F1: Ingreso manual de datos de cliente y pedido| B(P1: Gestión de Pedidos en Excel)
    C[Almacén / Producción] -->|F2: Consulta de stock y descuento de tela| D(P2: Control de Inventario en Excel)
    E[Plataforma Facturación Electrónica] <--|F3: Transcripción manual de totales| B
    
    B <-->|F4: Lectura y escritura concurrente| F[(D1: Disco Duro Local - Archivos Excel)]
    D <-->|F4: Lectura y escritura concurrente| F
    
    classDef boundary fill:none,stroke:#FF0000,stroke-width:2px,stroke-dasharray: 5 5;
    subgraph Red Local Insuclínicos
    B
    D
    F
    end
    class Red Local Insuclínicos boundary
