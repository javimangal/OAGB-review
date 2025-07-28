# One anastomosis gastric bypass (OAGB): Scoping review

This is a scoping review of one-anastomosis gastric bypass (OAGB), focusing on four key aspects: percentage excess weight loss (%EWL), remission of metabolic and cardiovascular comorbidities, postoperative complications, and incidence of gastroesophageal reflux disease (GERD).

## How to use

The suggested use of this repository starts with making sure that R and RStudio are installed in your computer:
1. Install [R and RStudio](https://posit.co/download/rstudio-desktop/) on your computer if you haven't done so. (Note that these analyses were conducted under R version 4.5.0 and RStudio 2025.05.0).
2. [Clone this repository](https://docs.github.com/en/repositories/creating-and-managing-repositories/cloning-a-repository). If you do not know how to do this, [you can follow these instructions](https://docs.github.com/en/desktop/overview/getting-started-with-github-desktop). Alternatively, you can [download the ZIP file](https://github.com/javimangal/OAGB-review/archive/refs/heads/main.zip), unpack it, and place it in a folder in your computer.
3. You should now have all these files in your computer with an identical folder structure (described in the following section).
4. In the main directory, open the file named ***OAGB-review.Rproj*** in RStudio.
5. You can navigate through the folders on the right-bottom panel of R Studio. Open the **R** folder. You should now see a series of files ending with ***.qmd***.
6. Open one of the .qmd files. You can run every chunk of code sequentially to reproduce the analyses. Make sure to respect the order and if something fails, I recommend that you start running al chunks of code from the beginning. If you don't know how to run a chunk of code, you can [imitate what this person is doing](https://youtu.be/RPF6gGyeJmg?feature=shared&t=30). If you get a message saying "Access denied", change from *Visual* to *Source* mode which can be done with the Ctrl+Shift+F4 command.
7. Please note that scripts are meant to be sourced into the flow of analyses in the main .qmd files. You may encounter problems if you attempt to run the scripts independently. 

If you are not able to follow the prior steps, you may also consider reviewing the [PDF reports](docs) documenting the analyses. 

-   [literature_search.qmd](R/literature_search.qmd). Documentation of search strategy in PubMed, Embase, and Web of Science. [PDF](docs/literature_search.docx)
-   [deduplication.qmd](R/deduplication.qmd). Main commented code file for deduplication with ASySD. [PDF](docs/deduplication.docx)

### ASReview 

You can access the exported asreview project files located in the **asreview** folder, which contain the records evaluated for this scoping review. These can be imported into ASReview by [following these instructions](https://asreview.readthedocs.io/en/latest/lab/manage.html).

## Project Structure

The project structure distinguishes three kinds of folders:
- read-only (RO): not edited by either code or researcher
- human-writeable (HW): edited by the researcher only.
- project-generated (PG): folders generated when running the code; these folders can be deleted or emptied and will be completely reconstituted as the project is run.


```
.
├── .gitignore
├── CITATION.cff
├── LICENSE
├── README.md
├── asreview           <- ASReview project files
├── data               <- All project data, ignored by git
│   ├── processed      <- The final, canonical data sets for modeling. (PG)
│   ├── raw            <- The original, immutable data dump. (RO)
│   └── temp           <- Intermediate data that has been transformed. (PG)
├── docs               <- Documentation notebook for users (HW)
│   ├── manuscript     <- Manuscript source, e.g., LaTeX, Markdown, etc. (HW)
│   └── reports        <- Other project reports and notebooks (e.g. Qmd, .Rmd) (HW)
├── results
│   ├── figures        <- Figures for the manuscript or reports (PG)
│   └── output         <- Other output for the manuscript or reports (PG)
└── R                  <- Source code for this project (HW)
    ├── scripts        <- Scripts sourced in main R markdown documents (PG)
    └── sessions       <- Text files with information of R sessions (PG)

```
## License

This project is licensed under the terms of the [MIT License](/LICENSE) by the authors. 

This project structure repository is adapted from the [Utrecht University simple R project template](https://github.com/UtrechtUniversity/simple-r-project), which builds upon the [Good Enough Project](https://github.com/bvreede/good-enough-project) Cookiecutter template by Barbara Vreede (2019).