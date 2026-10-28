# A/B Experiment Brief, RouteLogic (B2B)

## Parameters
| Parameter | Decision |
|---|---|
| Feature under test | Scaled down app for compliance checks to mark a delivery complete. |
| Persona | Delivery driver |
| Expected outcome | Increase in completed compliance checks. |
| Primary success metric | Compliance checks completed |
| Baseline rate | 64% |
| Guardrail metric | Compliance check utilization |
| Guardrail boundary | utilization must not drop below 50% |
| Second guardrail | · |
| Minimum Detectable Effect | +5% |
| Sample size per arm | 1,398 |
| Traffic split | · |
| Test duration | 14 days |
| Significance threshold | p < 0.05 |

## Control vs. Variant
- **Control (A):** The experience is having to check compliances through three different screens with a laggy experience.
- **Variant (B):** Cut down the compliance checks to one screen.
- **Held constant (isolation check):** The app has a home page that list the deliveries in order of completion.

## Hypothesis
> I believe that Scaled down app for compliance checks to mark a delivery complete. for Delivery driver will result in Increase in completed compliance checks., as measured by a +5% change in Compliance checks completed within 14 days. We will protect Compliance check utilization throughout the test.

## Shipping criteria
> We will **ship** if Compliance checks completed improves by ≥ +5% at p < 0.05 and Compliance check utilization does not reach utilization must not drop below 50% after 14 days.
> We will **iterate** if direction is positive but lift is below the MDE.
> We will **kill** if the primary metric shows no improvement or moves negatively.
> The read date is fixed at the end of 14 days, no results reviewed before this date.
