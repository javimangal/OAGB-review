# One anastomosis gastric bypass (OAGB): Scoping review

This is a scoping review of one-anastomosis gastric bypass (OAGB), focusing on four key aspects: percentage excess weight loss (%EWL), remission of metabolic and cardiovascular comorbidities, postoperative complications, and incidence of gastroesophageal reflux disease (GERD).

## Usage

In progress...

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