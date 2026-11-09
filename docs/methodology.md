# Methodology and Data Dictionary

## Scope
The report explores primary education access and equity from 2010 through 2023. 2023 is the benchmark/default year. The Year slicer allows exploration across the available period.

## Out-of-School Rate
Project notes describe the rate as:

`Out-of-school count / corresponding primary-school-age population × 100`

The result is on a 0–100 percentage scale. Exact DAX and denominator behavior must be confirmed against the model.

## Indicator Dictionary
| Indicator | Series code(s) | Meaning |
|---|---|---|
| Out-of-school children | `SE.PRM.UNER`; `SE.PRM.UNER.FE`; `SE.PRM.UNER.MA` | Counts, total and by sex |
| Primary-school-age population | `SAP.1`; `SAP.1.F`; `SAP.1.M` | Denominators for total and sex-disaggregated rates |
| Primary enrollment | `SE.PRM.ENRR`; `SE.PRM.ENRR.FE`; `SE.PRM.ENRR.MA` | Gross enrollment ratios; can exceed 100% |
| Primary completion | `SE.PRM.CMPT.ZS`; `SE.PRM.CMPT.FE.ZS`; `SE.PRM.CMPT.MA.ZS` | Completion rates, total and by sex |
| Gender parity index | `SE.ENR.PRIM.FM.ZS` | 1 indicates parity; below 1 boys ahead; above 1 girls ahead |
| Education expenditure | `SE.XPD.TOTL.GD.ZS` | Government education expenditure as % of GDP |
| Government effectiveness | `GE.EST` | Governance context indicator |

## Gender Gap
Project notes define Completion Gender Gap as male completion minus female completion. Positive values indicate a male advantage; negative values indicate a female advantage. Completion Gender Gap Magnitude represents absolute gap size. Confirm formulas in DAX before final publication.

## Interpretation
Education expenditure as a percentage of GDP is not per-student expenditure or a direct efficiency measure. Spending and governance scatterplots are exploratory and do not establish causation. Missing values are not zero.
