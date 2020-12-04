## Documentation as Code

* A través de `issues/merge` requests
* Usando control de versiones (Git)
* Archivos en texto plano (`Markdown`)
* Mediante colaboración y revisiones de código
* Implementando pruebas automatizadas (estilo, ortografía, links/imágenes)

---

## Ventajas

* Automatizado
* Control de cambios
* Feedback inmediato
* Facilita la revisión de los cambios
* Validación de estilo y standards de escritura
* URL's e imágenes siempre funcionando.

---

## Diagrama

```mermaid
graph LR;
    L[Laptop <br/> fa:fa-laptop] -- commit .md --> G[Gitlab <br/> fa:fa-git] --> a
    subgraph Pipeline
    a[HTML <br/> fa:fa-code ]-->b[Ortografía <br/> fa:fa-font]-->c[Estilo <br/> fa:fa-camera-retro ]
    end
    c-->P{Error fa:fa-question-circle};
    P -->|No| B[Gitlab Pages <br/> fa:fa-rocket];
    P -->|Si| A[Abort <br/> fa:fa-trash];
```

---

## Herramientas

* Hugo
* hugo-theme-learn
* Editor de Texto
* Gitlab

---

## Demo

* ¿Que vamos a ver?
* Estructura simple:

   ```text
   1. Empiece aquí
      * Instalación
         * Android
         * iOS
         * Linux
         * OSX
         * Windows
      * Configuración
   2. Ejemplos
   3. API
   4. Hacks
   ```
