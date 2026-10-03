# An Analysis of the Veteran Survival Dataset

A survival analysis of the veteran lung cancer dataset, written in Quarto and R. The project asks whether the treatment received (standard vs. test chemotherapy) affects survival, and whether patient characteristics such as tumour cell type are associated with survival time.

## Data

The analysis uses the `veteran` dataset, which ships with the R `survival` package. It comes from a randomised trial of two lung cancer treatments run by the US Veterans Administration. No data files are included in this repository, because the dataset loads automatically when the `survival` package is attached.

## Methods

- Kaplan-Meier estimation of survival curves
- Log-rank tests for comparing survival between groups
- Cox proportional hazards regression

No parametric survival models are used.

## Key findings

- The effect of treatment on survival probability is inconclusive.
- Differences in tumour cell type appear to have an effect on survival.

## Repository contents

| File | Description |
|------|-------------|
| `*.qmd` | Quarto source with the full analysis and write-up |
| `*.html` | Rendered report (download and open in a web browser) |
| `refs.bib` | Bibliography used by the report |
| `*.Rproj` | RStudio project file |

## How to reproduce

1. Install [R](https://www.r-project.org/), [RStudio](https://posit.co/download/rstudio-desktop/) (optional), and [Quarto](https://quarto.org/docs/get-started/).
2. Clone this repository and open the `.Rproj` file in RStudio.
3. Install the required packages. The `survival` package is needed for the data; check the `library()` calls at the top of the `.qmd` file for any others.

   ```r
   install.packages("survival")
   ```

4. Render the report:

   ```bash
   quarto render k_and_p_reanalysis.qmd
   ```

   or click **Render** in RStudio.

## License

Released under the MIT License. You are free to reuse and adapt this work.
