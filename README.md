# Práctica 3: Implementación de Pipeline CI/CD 🚀

**Estudiante:** Luis Kevin Díaz Piña  
**Asignatura:** DevOps (ITLA)  
**Proyecto:** API de Gestión de Tareas (Node.js/Express)

## 📋 Descripción del Proyecto
Este repositorio contiene la Práctica 3 de DevOps. Se trata de una aplicación web backend básica desarrollada en Node.js y Express, con pruebas automatizadas implementadas en Jest. 

El objetivo principal de este proyecto es demostrar la automatización de la integración continua (CI) y el despliegue continuo (CD) utilizando **GitHub Actions**.

## ⚙️ Estructura del Pipeline CI/CD
El pipeline (`.github/workflows/ci.yml`) se ejecuta automáticamente cada vez que se hace un `push` a la rama `main`. Consta de dos etapas (jobs) principales:

1. **Build and Test:**
   - Descarga el código fuente.
   - Configura el entorno con Node.js (v20).
   - Instala las dependencias mediante `npm ci`.
   - Ejecuta las pruebas unitarias y de integración con Jest (`npm test`).
   - Empaqueta la carpeta `/public` como artefacto.

2. **Deploy (GitHub Pages):**
   - Una vez que las pruebas pasan con éxito, toma el artefacto generado.
   - Despliega automáticamente los archivos estáticos a GitHub Pages.

## 🚀 Instrucciones de Despliegue Local

Si deseas ejecutar este proyecto en tu entorno local, sigue estos pasos:

1. **Clonar el repositorio:**
   ```bash
   git clone [https://github.com/LuisKevinDiaz/devops-practica3-itla.git](https://github.com/LuisKevinDiaz/devops-practica3-itla.git)
   cd devops-practica3-itla
