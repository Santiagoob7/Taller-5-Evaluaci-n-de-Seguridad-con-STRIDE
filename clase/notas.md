# 🗒️ Registro de Trabajo en Clase - Taller 5: Evaluación de Seguridad con STRIDE

## 📆 Fecha de la sesión
12 de septiembre de 2026

## 👥 Integrantes presentes
* Jorge Steven Doncel Bejarano — Código: 282296 / [gevengood](https://github.com/gevengood) / [jorgedobe@unisabana.edu.co](mailto:jorgedobe@unisabana.edu.co)
* David Santiago Buendia Londoño — Código: 306487 / [Santiagoob7](https://github.com/Santiagoob7) / [davidbulo@unisabana.edu.co](mailto:davidbulo@unisabana.edu.co)

## 🧠 Actividades realizadas en clase
Durante la sesión trabajamos en dos frentes complementarios:

1. **Análisis del caso base (EdukIT) y Reto OWASP Juice Shop:**
   * Analizamos el flujo de publicación de contenidos por docentes y acceso de estudiantes en la plataforma EdukIT.
   * Modelamos amenazas STRIDE sobre la autenticación de credenciales, peticiones de carga de cursos y base de datos relacional.
   * Documentamos el reto práctico de explotación de OWASP Juice Shop: Login Bypass mediante inyección SQL clásica (`' OR 1=1--`), identificando la ausencia de sentencias preparadas y consultas parametrizadas como la causa raíz.
   * Los resultados se consolidaron en la hoja `Tabla_STRIDE_EdukIT` del archivo [`clase/tabla-stride-clase.xlsx`](tabla-stride-clase.xlsx).

2. **Modelado de amenazas para el cliente real (Insuclínicos Ltda.):**
   * Delimitamos el alcance al núcleo operativo de la empresa: el PC de Administración, los archivos Excel (Pedidos e Inventario) y la comunicación por WhatsApp.
   * Se construyó el Diagrama de Flujo de Datos (DFD) en sintaxis Mermaid dentro del informe técnico, definiendo el límite de confianza alrededor de la red local.
   * Se identificaron 6 escenarios de riesgo específicos para una arquitectura de ofimática local (*Shadow IT*), destacando el disco duro local como punto único de falla (SPOF).
   * La matriz detallada de riesgos y mitigaciones se consignó en la hoja `Tabla_STRIDE_Insuclinicos` del archivo [`entrega/tabla-stride-cliente.xlsx`](../entrega/tabla-stride-cliente.xlsx).

## 🧩 Bocetos y entregables de clase
* [Tabla STRIDE Caso Base EdukIT y Reto OWASP (`clase/tabla-stride-clase.xlsx`)](tabla-stride-clase.xlsx)
* [Guía Paso a Paso de STRIDE (`clase/guia_paso_a_paso_stride.md`)](guia_paso_a_paso_stride.md)
* [Visualización Interactiva de Modelado de Amenazas (`clase/modelado-de-amenazas.html`)](modelado-de-amenazas.html)

## 🔁 Tareas definidas para la entrega final

| Tarea asignada | Responsable | Fecha estimada |
|:---|:---|:---:|
| Consolidación de la matriz STRIDE para EdukIT y registro del reto OWASP | Jorge Doncel | 12/09/2026 |
| Estructuración del DFD en código Mermaid y tabla de amenazas de Insuclínicos | David Buendia | 12/09/2026 |
| Redacción técnica de mitigaciones, investigación CISA/NIST y referencias APA | Jorge Doncel | 13/09/2026 |
| Revisión cruzada de hojas de cálculo y control de calidad del repositorio | Ambos | 13/09/2026 |

---

_Este documento resume el trabajo colaborativo realizado durante la sesión del Taller 5 en el curso AREM — Universidad de La Sabana._
