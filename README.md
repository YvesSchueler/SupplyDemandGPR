# Supply and demand geopolitical risk (GPR) indices

Monthly supply-type and demand-type geopolitical risk indices for the United States, 1985:1–2026:3, from

> Schüler, Y., Arndt, S., Bondarenko, Y., Lewis, V., and Rottner, M. (2026). *Coherent shocks: External identification and internal validation with an application to geopolitical risk*. CEPR Discussion Paper 21794. [cepr.org/publications/dp21794](https://cepr.org/publications/dp21794)

Please cite the paper when using the data.

## Data

**`SupplyDemandGPR.xlsx`** — sheet `Data` contains

| column | description |
|---|---|
| `month` | first day of the month |
| `supply_gpr` | supply-type GPR index, mean 100 over 1985:1–2026:3 |
| `demand_gpr` | demand-type GPR index, mean 100 over 1985:1–2026:3 |

Permalink to the latest vintage:
`https://github.com/YvesSchueler/SupplyDemandGPR/raw/main/SupplyDemandGPR.xlsx`

## What the indices measure

The Caldara–Iacoviello (2022) GPR index is topic-defined: it counts newspaper articles about geopolitical risk without regard to how the event is reported to affect the economy. The two indices here split that coverage by economic mechanism.

- **Supply GPR**: articles that explicitly link a geopolitical event to supply disruptions or rising costs/prices for the U.S. economy.
- **Demand GPR**: articles that explicitly link a geopolitical event to falling U.S. consumer, business, or investor confidence, or falling demand for goods and services.

Articles are retrieved from Factiva Analytics with the Caldara–Iacoviello search query (USA Today, Chicago Tribune, The Globe and Mail, The Daily Telegraph, The Guardian, The Wall Street Journal, The Washington Post) and classified by a large language model (GPT-4.1-nano, temperature zero) answering a fixed yes/no questionnaire; only high-likelihood classifications are retained. The questionnaire is reproduced in `questionnaire.txt`. Each index is the share of classified articles in the total corpus, normalized to a mean of 100.

The indices are overlapping subindices of the Caldara–Iacoviello index: an article describing both mechanisms enters both, and the two do not sum to the overall index. Events such as 9/11 load mainly on the demand index; the Gulf War, Russia's invasion of Ukraine, and the 2026 Middle East conflict load mainly on the supply index. The two indices correlate at about 0.3.

Because the classification uses no macroeconomic data, the indices can be constructed in real time as events unfold.

## Updates

The indices are updated periodically. The vintage is stated in the `Readme` sheet of the Excel file and in the commit history.

## Contact

Yves Schüler, Deutsche Bundesbank — yves.schueler (at) bundesbank.de

The views expressed are those of the authors and do not necessarily coincide with the views of the Deutsche Bundesbank, the European Central Bank, the Bank for International Settlements, or the Eurosystem.
