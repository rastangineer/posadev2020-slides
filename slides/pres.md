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

![diagrama](/slides/diagrama.png)

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

--

1. Crear repo `asistente` usando **pages/hugo** templates
2. Clonar repo en `vscode` (configurar ssh primero)
   * ⚠️ no olvidar

     ```bash
     $ git config user.email kike.cuevas@gmail.com
     $ git config user.name rastangineer
     ```

3. Revisar `gitlab-ci.yml`
4. Edit `config.toml`
   * Agregar

     ```toml
     baseurl = "https://rastangineer.gitlab.io/asistente/"
     title = "Asistente"
     ```

--

5. Revisar `Settings -> Pages` y abrir url.
6. Instalar [hugo-learn-theme](https://themes.gohugo.io//theme/hugo-theme-learn/en) (búsqueda, soporte multi-idiomas, botones navegación, adjuntar archivos, diagramas mermaid)
   * Agregar submodule
      `git submodule add https://github.com/matcornic/hugo-theme-learn.git themes/hugo-theme-learn`
   * Modificar `config.toml`

      ```toml
      theme = "hugo-theme-learn"
      ```

   * ⚠️ El pipeline fallará porque existen algunos archivo `markdown` del tema anterior que no son compatibles con el nuevo tema. Hay que borrarlos

      ```log
      Error: Error building site: "/builds/rastangineer/asistente/content/post/2017-03-20-photoswipe-gallery-sample.md:10:1": failed to extract shortcode: template for shortcode "gallery" not found
      ```

--

7. Arreglar el tema:
   * El tema seleccionado  
   * Borrar las carpetas:
     * `content/post/`
     * `content/page/`
     * `themes/beautifulhugo`
     * `themes/Lanyon`
8. Cambiar logo
   * Crear archivo `layouts/partials/logo.html` y agregar

      ```html
      <a href="/">
         <img src="/logo.png" alt="logo.png">
      </a>
      ```

   * Copiar `logo.png` en la carpeta `static/`
   * Cambiar color del tema:

      ```toml
      [Params]
         # Change default color scheme with a variant one. Can be "red", "blue", "green".
         themeVariant = "green"
      ```
