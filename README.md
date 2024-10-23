# `calliope-tutorial`

## Getting started

Follow these [installation instructions](https://github.com/sjpfenninger/optimisation-course/blob/main/README.md) to set up a Python environment with everything necessary installed.

Inside a Jupyter Notebook, you can run a model with these two lines of code - the `!` means execution of a tool outside of Python, and you could also run these two commands (without the `!` in a terminal or shell window if you prefer that):

```bash
!calliope run economic_dispatch/model.yaml --save_netcdf results_economic_dispatch.nc
!calligraph results_economic_dispatch.nc
```

## Exercise questions

### Exercise 1. City-scale dispatch problem

Assume we are modelling for city A that has gas power plants and a nuclear power plan with fixed total capacity. To meet the electricity demand of the city, the above-mentioned power plants and some renewable energy plants are in use.

**Step 1**. Run model 1 without any renewables capacity, then use calligraph to plot the results. Navigate to Timeseries plots, and choose 'flow*' in the drop-down list of Variable. Then, at the bottom of the page, choose 'Original resolution'.
1. What do you observe as the dispatch pattern between gas and nuclear power plants?
2. What is the electricity shadow price, and can you explain why it is at this value?

**Step 2**. Run model 1 and add 3 GW of onshore wind and 3 GW of solar in `model_1/input/nodes.yaml`. Plot the results again.
1. What happens to the shadow price now? Why is it?
2. What have you observed regarding the operation curves of wind and solar?

### Exercise 2. Intercountry capacity expansion problem

Assume we are modelling three countries: Germany, Switzerland and Italy. Each country has certain amount of available land for renewables with different capacity factors.

**Step 1.** Run model 2 as it sits now. In this setting, no transmission capacity between countries is allowed, and it is also not possible to have any storage technology. Observe the capacity of different technologies as well as the dispatch plots in each country.
1. What do you think of the efficiency of resource utilisation? Why?

**Step 2.** Remove the limit of maximum transmission capacity for each transmission link and rerun the model. Observe the capacity and dispatch plots again.
1. What has changed in terms of technology capacities? Why do you think the model makes this choice?
2. What exactly happens as shown in the dispatch plot (where is importing, where is exporting, and when is that happening)?

**Step 3.** Remove the limit of maximum storage (in this case, battery) capacity and rerun the model. Observe the capacity and dispatch plots again.
1. What has changed in terms of technology capacities? Why do you think the model makes this choice?
2. Could you give an overview of the effects of transmission and storage technologies in the whole energy system (especially with a high renewables share)?
