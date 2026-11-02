# The Oswego church supper, 1940

A worked-example repository for [Fieldwork](https://github.com/digital-twin-ph/fieldwork). It carries
the line list from a classic outbreak investigation, with its provenance and its limits.

On 18 April 1940 a church supper was held in **Lycoming**, a small village in Oswego County, New York,
2 miles from Lake Ontario. Most of those who attended became ill that night. "Oswego" is the name of
the teaching problem, not the place. The case has been used to train epidemiologists since 1940.

**No study design is declared here.** The table comes first, so a practitioner can work from the
counts to a declaration. As a retrospective comparison of everyone at one meal, it reads as a cohort,
and that reading is left for the practitioner to argue.

## The line list

[`data/oswego-line-list.csv`](data/oswego-line-list.csv) has one row per person: 75 people, 46 of them
ill. Columns are as CDC's table spells them.

| In the file | Means |
| --- | --- |
| `unk` in `Time of meal` | Not known |
| `?` in a food column | Not known. Two cells: person 19 for mashed potato, person 44 for chocolate ice cream |
| `12:00 AM*` | Midnight between 4/18 and 4/19, as CDC's footnote says |
| Empty onset | The person was not ill |

## Food-specific attack rates

Worked out from the file. Blanks are left out, not counted as "did not eat".

| Food | Ate: ill / all | Attack rate | Did not eat: ill / all | Attack rate |
| --- | ---: | ---: | ---: | ---: |
| Baked ham | 29 / 46 | 63% | 17 / 29 | 59% |
| Spinach | 26 / 43 | 60% | 20 / 32 | 62% |
| Mashed potato | 23 / 37 | 62% | 23 / 37 | 62% |
| Cabbage salad | 18 / 28 | 64% | 28 / 47 | 60% |
| Jello | 16 / 23 | 70% | 30 / 52 | 58% |
| Rolls | 21 / 37 | 57% | 25 / 38 | 66% |
| Brown bread | 18 / 27 | 67% | 28 / 48 | 58% |
| Milk | 2 / 4 | 50% | 44 / 71 | 62% |
| Coffee | 19 / 31 | 61% | 27 / 44 | 61% |
| Water | 13 / 24 | 54% | 33 / 51 | 65% |
| Cakes | 27 / 40 | 68% | 19 / 35 | 54% |
| **Ice cream (vanilla)** | **43 / 54** | **80%** | **3 / 21** | **14%** |
| Ice cream (chocolate) | 25 / 47 | 53% | 20 / 27 | 74% |
| Fruit salad | 4 / 6 | 67% | 42 / 69 | 61% |

Gross's 1976 table gives 21 ill among those who did not eat chocolate ice cream, where this table
gives 20. Person 44 was ill and chocolate ice cream is `?`, which would account for the difference.
Gross prints 67% for cakes, where 27 of 40 rounds to 68%.

## What the investigation found

Vanilla ice cream was implicated by food histories and by culture, and the agent was *Staphylococcus
aureus*. The mixes were prepared on 17 April and left covered at room temperature overnight before
freezing.

No source of contamination was established in 1940. In 1972 Michael Gross interviewed surviving
principals. The village health officer recalled that one maker of the ice cream had shown a small,
draining infection on a finger the morning after the supper. It was never cultured or recorded, and
the people who made the ice cream did not recall it. That is a hypothesis and not a finding.

## What this does not establish

- **Five people are missing.** 80 attended and 75 were interviewed. Attack rates here are of those
  interviewed.
- **Meal time is known for 22 of the 46 who were ill,** so an incubation period rests on those 22.
  Their median is 4 hours, computed here.
- **Three people who were ill report no vanilla ice cream:** persons 9, 39 and 59. The file does not
  say why.
- **Exposure is by recall,** collected from 20 April onward.
- **This repository has no coordinates.** The setting is named and not located, so no map is carried
  yet.
- **No Fieldwork project is included yet.** The workflow has not been built or run in the application.

## Sources

- Centers for Disease Control and Prevention, Epidemiology Program Office. *Oswego: An Outbreak of
  Gastrointestinal Illness Following a Church Supper.* Case Studies in Applied Epidemiology, No.
  401-303, Student's Guide. <https://www.cdc.gov/eis/downloads/xoswego-401-303-student.pdf>
- Gross M. Oswego County revisited. *Public Health Reports* 1976; March-April: 168-170.
  <https://stacks.cdc.gov/view/cdc/65198/cdc_65198_DS1.pdf>

The line list was checked against the `oswego` data in the R package
[epitools](https://cran.r-project.org/web/packages/epitools/index.html) 0.5-10.1. See
[`provenance.json`](provenance.json) and [`NOTICE.txt`](NOTICE.txt).
