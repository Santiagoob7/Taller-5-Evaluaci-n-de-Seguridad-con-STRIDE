# 🛡️ Taller 5: Evaluación de Seguridad con STRIDE

**Cliente:** Insuclínicos Ltda.  
**Curso:** Arquitectura Empresarial (AREM) — Universidad de La Sabana  

## 👥 Equipo de Trabajo
* **Jorge Steven Doncel Bejarano** — [gevengood](https://github.com/gevengood)
* **David Santiago Buendia Londoño** — [Santiagoob7](https://github.com/Santiagoob7)

## 🧠 Descripción del Proyecto
Este repositorio contiene el desarrollo del Taller 5 de Arquitectura Empresarial, enfocado en el modelado de amenazas mediante el marco **STRIDE** (*Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, Elevation of Privilege*). 

El trabajo se divide en dos fases:
1. **Trabajo en Clase (`clase/`):** Análisis del sistema de referencia (**EdukIT**) y documentación del reto práctico de explotación (**OWASP Juice Shop** — Login Bypass por SQLi).
2. **Aplicación al Cliente Real (`entrega/`):** Evaluación de seguridad de la arquitectura actual (AS-IS) de **Insuclínicos Ltda.**, centrada en el flujo de gestión operativa (Archivos Excel locales y WhatsApp) que soporta los pedidos y el inventario.

## 📁 Estructura del Repositorio

```text
taller-05-seguridad-stride/
├── README.md
├── clase/
│   ├── guia_paso_a_paso_stride.md      # Categorías STRIDE, metodología de 5 pasos y ejemplo guiado
│   ├── modelado-de-amenazas.html       # Visualización interactiva del modelado de amenazas
│   ├── stride_analisis_ejemplos.xlsx   # Banco de 10 amenazas STRIDE de ejemplo
│   ├── tabla-stride-clase.xlsx         # Tabla STRIDE aplicada a EdukIT y reto OWASP
│   └── notas.md                        # Registro de trabajo colaborativo en clase
├── entrega/
│   ├── tabla-stride-cliente.xlsx       # Matriz STRIDE aplicada a Insuclínicos Ltda.
│   ├── informe.md                      # Informe técnico, tabla de riesgo, DFD Mermaid e investigación
│   └── referencias.md                  # Bibliografía y normativas de seguridad (CISA, OWASP, NIST)
└── plantillas/
    ├── plantilla_analisis_stride.xlsx
    ├── plantilla_informe_taller.md
    ├── plantilla_notas.md
    └── plantilla_referencias.md
```

## 📄 Entregables Principales

| Entregable | Ruta | Descripción |
|---|---|---|
| **Informe Técnico STRIDE** | [`entrega/informe.md`](entrega/informe.md) | Metodología de 5 pasos, DFD en Mermaid, análisis de amenazas e investigación complementaria |
| **Matriz STRIDE Cliente** | [`entrega/tabla-stride-cliente.xlsx`](entrega/tabla-stride-cliente.xlsx) | 6 escenarios STRIDE evaluados para Insuclínicos con impacto, controles y mitigación |
| **Referencias Bibliográficas** | [`entrega/referencias.md`](entrega/referencias.md) | Fuentes técnicas (Microsoft STRIDE, CISA 3-2-1, OWASP Top 10, Windows Security) |
| **Matriz STRIDE Clase** | [`clase/tabla-stride-clase.xlsx`](clase/tabla-stride-clase.xlsx) | Análisis de EdukIT y reto de explotación en OWASP Juice Shop |
| **Notas de Clase** | [`clase/notas.md`](clase/notas.md) | Bitácora de trabajo colaborativo y decisiones del equipo |
