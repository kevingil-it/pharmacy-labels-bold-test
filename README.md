# The Pharmacy Hub — Label Center

Paquete para GitHub Pages / GitHub Pages package · 2026-11-10

Label Center 1.5 · Motivated 2.4.4 · Cottonball 2.4.5 · Manual 1.8

## Español

Esta entrega corrige el catálogo de Cottonball y bloquea fechas inválidas o
invertidas en ambos programas. La portada, las fuentes, la geometría y los
ajustes de impresión conservan su comportamiento anterior. Los archivos HTML contienen las fuentes, las imágenes
y el generador QR. No requieren instalación, compilación, Vercel ni un servidor
de aplicaciones.

### Publicar en el repositorio de Iván

1. Descomprime el ZIP. Conserva una copia de los archivos que ya tenga el
   repositorio antes de reemplazarlos.
2. En GitHub, abre el repositorio y selecciona **Add file → Upload files**.
   Sube **todos los archivos extraídos**, no el ZIP ni una carpeta que los
   encierre. `index.html` debe quedar directamente en la carpeta que publica
   Pages, junto con `motivated-labels.html` y `cottonball-labels.html`.
3. Confirma la subida con **Commit changes**. En una publicación desde la raíz,
   este `index.html` sustituye la portada anterior del repositorio.
4. Si Pages ya está configurado, conserva su rama y carpeta de publicación y
   comprueba que subiste allí los archivos. Si aún no está configurado, entra
   en **Settings → Pages → Build and deployment**, elige **Deploy from a
   branch**, la rama que contiene los archivos (normalmente `main`) y
   **/(root)**. Pulsa **Save**. Para usar Pages con GitHub Free, el repositorio
   debe ser público.
5. Espera a que finalice correctamente el despliegue en **Actions**. Abre el
   enlace que aparece en **Settings → Pages → Visit site** y prueba los dos
   botones de clínica. Comparte ese enlace, no la dirección del repositorio.

Los enlaces son relativos: el nombre del repositorio y la cuenta pueden ser
distintos sin editar el código. Conserva exactamente los nombres y las
mayúsculas de los archivos. Si el repositorio publica desde `/docs`, sube los
archivos a esa carpeta; no cambies su configuración a raíz sin trasladarlos.
Si utiliza un flujo de Actions propio, ese flujo debe publicar estos archivos
con `index.html` en la raíz de su artefacto.

Guía oficial de publicación:
[Configurar el origen de GitHub Pages](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

### Uso y datos guardados

Abre Label Center, selecciona la clínica y prepara la orden dentro de su
programa. Para imprimir usa **Print labels**. El manual completo está en
[Documentation-ES-EN.html](Documentation-ES-EN.html).

El ZIP incluye el catálogo inicial incorporado al código. Los medicamentos
añadidos desde la interfaz, las contraseñas del catálogo y los perfiles de
impresora guardados en un navegador no viajan dentro del ZIP ni se comparten
automáticamente entre equipos. Un dominio nuevo puede usar otro almacenamiento.
Exporta el perfil de la estación anterior con **Export printer profile** e
impórtalo en la nueva ubicación si corresponde a esa misma impresora. El
catálogo personalizado requiere una transferencia independiente; el programa
no incluye un botón de exportación/importación del catálogo. El CSV incluido
es una referencia, no una herramienta de importación.

Antes de una tanda en una estación nueva, verifica una etiqueta impresa, el
contenido completo del QR y la alineación. Las comprobaciones del paquete no
sustituyen esa prueba física. Para una revisión local puedes abrir `index.html`
después de extraer todos los archivos; verifica el uso final desde Pages.

### Archivos

| Archivo | Función |
| --- | --- |
| `index.html` | Portada con los enlaces a las dos clínicas. |
| `motivated-labels.html` | Programa de Motivated. |
| `cottonball-labels.html` | Programa de Cottonball. |
| `compound-labels-NEW.html` | Redirección para conservar el enlace antiguo de Motivated. |
| `Documentation-ES-EN.html` | Manual completo: uso, impresión, QR, perfiles, catálogo y mapa del código. |
| `START-HERE-ES-EN.txt` | Inicio rápido en español e inglés. |
| `MAINTENANCE-ES-EN.txt` | Estructura del código y pautas para futuras actualizaciones. |
| `cottonball-catalog-reference.csv` | Referencia de las fórmulas iniciales de Cottonball. |
| `Verification-Results.json` | Comprobaciones del paquete y evidencia histórica identificada. |
| `Catalog-Audit.html` | Auditoría de los 32 PDF de Cottonball, duplicados, discrepancias y alcance. |
| `Catalog-Audit.csv` | Relación de cada PDF con el catálogo corregido. |
| `Catalog-Date-Verification.json` | Resultados de las pruebas de fechas, catálogo y salida de 67 etiquetas. |
| `SHA256SUMS.txt` | Huellas de los archivos para comprobar su integridad. |
| `README.md` | Estas instrucciones. |

Si aparece un 404, revisa la rama y carpeta elegidas en Pages y comprueba que
`index.html` está allí, con ese nombre exacto. Si ves una copia anterior,
confirma el despliegue antes de recargar la página; no borres los datos del
navegador como primer paso, porque contienen ajustes y catálogo local.

## English

This release reconciles the Cottonball catalog and blocks invalid or reversed
dates in both applications. The landing page, fonts, label geometry and printer
settings retain their previous behavior. Fonts, images and the QR encoder are embedded
in the HTML files. No installation, build, Vercel or application server is
required.

### Publish in Iván’s repository

1. Extract the ZIP. Back up any existing repository files before replacing them.
2. Open the GitHub repository and select **Add file → Upload files**. Upload
   **all extracted files**, not the ZIP or an enclosing folder. `index.html`
   must be directly in the Pages publishing folder, alongside
   `motivated-labels.html` and `cottonball-labels.html`.
3. Select **Commit changes**. When publishing from the repository root, this
   `index.html` replaces the previous landing page.
4. If Pages is already configured, retain its publishing branch and folder
   and upload the files there. Otherwise, open **Settings → Pages → Build and
   deployment**, select **Deploy from a branch**, choose the branch containing
   the files (usually `main`) and **/(root)**, then **Save**. GitHub Free requires
   a public repository for Pages.
5. Wait for the deployment in **Actions** to succeed. Open **Settings → Pages
   → Visit site**, check both clinic buttons, and share that website URL rather
   than the repository URL.

Links are relative, so a different owner or repository name requires no code
changes. Keep filenames and capitalization exactly as supplied. If Pages
publishes from `/docs`, upload the files there. If a custom Actions workflow
is used, it must publish these files with `index.html` at its artifact root.

Official setup guide:
[Configure a GitHub Pages publishing source](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site).

### Use and saved data

Open Label Center, select a clinic and prepare the order in its application.
Use **Print labels** to print. See [Documentation-ES-EN.html](Documentation-ES-EN.html)
for the complete bilingual manual.

The ZIP includes the initial catalog embedded in the code. Medications added
through the interface, catalog passwords and saved printer profiles remain
in each browser; they are not included in this ZIP or automatically shared
between computers. A different domain may use different storage. Use **Export
printer profile** at the previous location and import that profile at the new
location if it belongs to the same printer. Custom catalogs need a separate
transfer; the applications have no catalog export/import button. The included
CSV is a reference, not an import tool.

On a new workstation, verify one printed label, its full scanned QR content
and alignment before running a batch. Package checks do not replace a physical
print test. You can open `index.html` locally after extracting all files, but
verify the final setup from Pages.

### Files

| File | Purpose |
| --- | --- |
| `index.html` | Landing page with two clinic links. |
| `motivated-labels.html` | Motivated application. |
| `cottonball-labels.html` | Cottonball application. |
| `compound-labels-NEW.html` | Compatibility redirect for the old Motivated URL. |
| `Documentation-ES-EN.html` | Full user and technical manual in both languages. |
| `START-HERE-ES-EN.txt` | Bilingual quick start. |
| `MAINTENANCE-ES-EN.txt` | Code structure and update guidance. |
| `cottonball-catalog-reference.csv` | Initial Cottonball formula reference. |
| `Verification-Results.json` | Package checks and identified historical evidence. |
| `Catalog-Audit.html` | Full 32-PDF Cottonball audit, discrepancies and scope. |
| `Catalog-Audit.csv` | Source-to-catalog reconciliation. |
| `Catalog-Date-Verification.json` | Date, catalog migration and 67-label output checks. |
| `SHA256SUMS.txt` | File integrity hashes. |
| `README.md` | These instructions. |

For a 404, check the selected branch/folder and the exact `index.html` filename.
For an older page, confirm deployment success before reloading. Do not clear
browser storage as a first step: it contains local settings and catalogs.


## Release notes · 2026-11-10

**Español.** Los cambios del catálogo y de fechas pertenecen a los programas
oficiales, no solo a una copia de pruebas. Los 32 PDF de Cottonball contienen
31 combinaciones distintas de variante, ingredientes y concentraciones. Las
dos entradas CX.1 Resistant se consolidan conservando el QR de la entrada
canónica. Las fórmulas personalizadas no se fusionan automáticamente; se
conservan y se señalan para revisión. La migración conserva la contraseña y
archiva la entrada original retirada en el mismo registro local.

Ambas fechas son obligatorias y deben existir en el calendario. BUD no puede
ser anterior a la fecha de preparación; el mismo día se permite. No se
intercambian fechas automáticamente ni se calcula una vida útil clínica.
La aplicación bloquea la etiqueta inválida en impresión y exportación; no
puede impedir que el navegador abra su propio diálogo de impresión.

Se verificaron 67 casos válidos con salida idéntica a la versión anterior,
24 casos de fechas y ocho escenarios de catálogo. No hubo prueba física de
impresora. El informe distingue el catálogo Cottonball verificado contra PDF
de Motivated, cuyos 18 nombres se compararon con los HTML disponibles, sin
un conjunto independiente de PDF de fórmulas. Incluye dos discrepancias de
origen pendientes de revisión; sus concentraciones no se modificaron.

Este paquete no contiene los programas de prueba de calibración. Publicar
estos archivos actualiza los programas oficiales. La preparación del ZIP
por sí sola no actualiza el sitio público.

**English.** Catalog and date corrections apply to the official applications.
The 32 Cottonball PDFs represent 31 distinct variant/ingredient/strength
combinations. The two CX.1 Resistant entries are consolidated while retaining
the canonical entry's QR payload. Custom formulas are preserved for review,
not automatically merged. Migration retains authentication and archives the
retired original entry in the same local record.

Both dates are required and must be valid calendar dates. BUD cannot precede
preparation; same-day dates remain allowed. Dates are never silently swapped,
and the software does not calculate clinical shelf life. Invalid labels are
blocked from printing and export; the browser's own print dialog may still open.

Verification covers 67 valid outputs unchanged from the prior release,
24 date cases and eight catalog scenarios. No physical printer was tested.
The audit distinguishes Cottonball's PDF-verified catalog from Motivated's
18 names checked against available HTML catalogs, without an independent
formula-PDF set. Two source discrepancies remain for review; concentrations
have not been altered.

Calibration test copies are distributed separately. Publishing these release
files updates the official applications; preparing this ZIP does not itself
update the public site.
