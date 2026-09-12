# 🗒️ Registro de Trabajo en Clase - Taller 5

## 📆 Fecha de la sesión
12 de septiembre de 2026

## 👥 Integrantes presentes
* espacio jorge
* David Santiago Buendia Londoño

## 🧠 Actividades realizadas en clase
Durante la sesión trabajamos en dos frentes (EdukIT e Insuclínicos Ltda.):
1. **Análisis de EdukIT:** Seleccionamos el flujo de publicación de contenidos por docentes. Discutimos cómo la falta de controles en la subida de archivos y la validación de roles en el frontend representan riesgos críticos. 
2. **Reto OWASP Juice Shop:** Tuvimos inconvenientes técnicos con el contenedor de Docker y la caída de la instancia pública de Heroku de OWASP. Para no bloquear el avance, documentamos teóricamente el payload del reto de Login Bypass (`' OR 1=1--`), identificando la vulnerabilidad subyacente (falta de consultas parametrizadas).
3. **Análisis del Cliente Real (Insuclínicos):** Acordamos que el análisis no podía enfocarse en una arquitectura web porque la empresa opera con ofimática local. Decidimos dibujar el DFD centrado en el PC de Administración y sus archivos Excel.
4. **Herramientas:** Utilizamos sintaxis Mermaid para renderizar el diagrama de flujo de datos directamente en GitHub sin depender de imágenes externas.

## 🧩 Boceto inicial del modelo
El modelo conceptual inicial se centró en identificar el "Punto Único de Falla". Determinamos que el disco duro local donde reposa el Excel maestro era el activo más crítico (D1), delimitando nuestro límite de confianza alrededor de la red local de la empresa. *(El diagrama final codificado en Mermaid se encuentra en el archivo informe.md de la entrega final).*

## 🔁 Tareas definidas para complementar el taller

| Tarea asignada | Responsable | Fecha estimada |
| :--- | :--- | :--- |
| Consolidación de la matriz STRIDE para EdukIT y registro del reto OWASP en Excel | Jorge Doncel | 12/09 |
| Estructuración del DFD en código Mermaid y redacción de amenazas en el contexto ofimático de Insuclínicos | David Buendia | 12/09 |
| Redacción del informe final, búsqueda de normativas CISA/OWASP y consolidación del repositorio | Ambos | 12/09 |
