# Plantilla de Proyecto de R

Esta plantilla de proyectos de R ha sido modificada para contener personalizaciones mayores respecto a la [plantilla original](https://github.com/UtrechtUniversity/simple-r-project) utilizada.

## Uso 

1.  Verifica que ya tengas instaladas las últimas versiones de R y RStudio. Las instrucciones de descarga [se encuentran en esta liga](https://posit.co/download/rstudio-desktop/). Sigue los pasos 1 y 2 de la página. 
2.  Ahora, puedes [descargar el archivo .ZIP de este repositorio](https://github.com/javimangal/mklab-plantilla/archive/refs/heads/main.zip), descomprimirlo y colocarlo la carpeta en un directorio de tu conveniencia en tu computadora personal.
3.  Cambia el nombre de la carpeta por uno nuevo para tu proyecto, al igual que el nombre del archivo con extensión **.Rproj**. Por ejemplo, si tu nuevo proyecto es sobre **cefalea en estudiantes de medicina**, un buen nombre para tu proyecto debería ser simple y representativo (ej. ***cefalea-facmed***). Ahora, puedes sustituir el nombre de la carpeta por cefalea-facmed y el nombre del archivo de proyecto de R a **cefalea-facmed.Rproj**.
4.  Haz doble click sobre el archivo con terminación **.Rproj**. Esto inicializará RStudio y automáticamente establecerá tu carpeta de trabajo (working directory) en donde se encuentra el archivo **.Rproj**. Gracias a esto, ya no tendrás que preocuparte por indicar el directorio de trabajo cada que trabajes en tu proyecto.
5.  ¡Estás listo para trabajar en tu proyecto de R!
6.  Este proyecto utiliza documentos de quarto (.qmd) para combinar texto libre y código de R. Se utilizan rutas relativas para leer y escribir archivos en las distintas carpetas del proyecto. Los scripts de R se colocan dentro del directorio R/scripts y son leídos dentro del flujo de trabajo de los documentos qmd. Para más información sobre este tipo de documentos, [puedes consultar esta liga](https://quarto.org/docs/computations/r.html). 

Sugerencia: Puedes crear un nuevo repositorio público o privado desde la carpeta de tu nuevo proyecto por medio de [GitHub Desktop](https://docs.github.com/es/desktop/adding-and-cloning-repositories/adding-a-repository-from-your-local-computer-to-github-desktop) para comenzar a tomar provecho del control de cambios de versiones de git y el respaldo de tu proyecto y colaboración por medio de GitHub. 

## Estructura del Proyecto

La estructura del proyecto distingue tres tipos de carpetas:
- sólo lectura (RO): archivos que no son editados por el autor ni modificados por el código.
- editable por humano (HW): Archivos editados sólo por el autor.
- project-generated (PG): carpetas que se generan al correr el código; estos pueden ser vaciados o eliminados y ser completamente reconstituidos al correr el código del proyecto.

```         
.
├── .gitignore
├── CITATION.cff
├── LICENSE
├── README.md
├── mklab-plantilla.Rproj
├── data                  <- All project data files
│   ├── processed         <- The final, canonical data sets for modeling. (PG)
│   ├── raw               <- The original, immutable data. (RO)
│   └── temp              <- Intermediate data that has been transformed. (PG)
├── docs                  <- Documentation for users (HW)
│   ├── manuscript        <- Manuscript source, docx. (HW)
│   ├── presentations     <- Presentations, pptx, pdf. (HW)
│   ├── reports           <- Project reports, pdf. (HW)
│   └── DAG               <- Directed Acyclic Graph documentation, txt. (HG)
├── results
│   ├── output_figures    <- Figures for the manuscript or reports (PG)
│   └── output_tables     <- Output tables for the manuscript (PG)
└── R                     <- Source code for this project (HW)
    ├── scripts           <- Scripts sourced in main R markdown documents (PG)
    └── sessions          <- Text files with information of R sessions (PG)

```

## Edita el archivo de cita, licencia y gitignore

Puedes editar el archivo de cita para este repositorio [CITATION.cff](/CITATION.cff) siguiendo [estas recomendaciones](https://docs.github.com/es/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/about-citation-files).

Se ha incluido una licencia tipo MIT, que es permisiva. Si deseas conservar este tipo de licencia, recuerda cambiar tu nombre en la licencia de tu nuevo repositorio. Si deseas consultar otro tipo de licencias que se ajusten a tus necesidades, puedes [consultar esta página](https://docs.github.com/es/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository). 

El archivo [gitignore](/.gitignore) contiene instrucciones sobre los archivos que no deseas que sean rastreados ni publicados en tu repositorio de GitHub. Recomiendo usar las instrucciones default para un proyecto de R, sin embargo, puedes editar el tipo de archivos que deseas que sean visibles. Por ejemplo, la opción default es siempre ignorar el rastreo y publicación de datos por seguridad. Sin embargo, si deseas publicar tus datos y estás seguro de que no cometes el riesgo de publicar datos sensibles, puedes borrar los directorios referentes a datos dentro del archivo gitignore para hacerlos públicos. 

## Licencia y Créditos   

El uso de este proyecto está permitido mediante los términos de la [licencia MIT](/LICENSE).

Esta plantilla de proyectos ha sido adaptada a partir la plantilla [simple-r-project](https://github.com/UtrechtUniversity/simple-r-project), que utiliza la estructura de proyectos [Good Enough Project](https://github.com/bvreede/good-enough-project) de Barbara Vreede (2019). Ambos proyectos están disponibles bajo una licencia MIT, las cuales pueden ser consultadas [aquí](https://github.com/UtrechtUniversity/simple-r-project/blob/main/LICENSE) y [aquí](https://github.com/bvreede/good-enough-project/blob/master/LICENSE.md).
