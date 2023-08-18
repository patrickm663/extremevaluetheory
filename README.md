# Extreme Value Theory
**_This investigation is currently a WIP_**

A demonstration Extreme Value Theory (EVT) using the Block Maxima method with Bayesian sampling in Julia.

## Approach
This repo makes use of the `battery` water levels dataset found in the `pyextremes` package. It takes the annual maximum water elevation level and fits a Generalised Extreme Value (GEV) to the observations.

Bayesian methods allow us to produce uncertainty quantifications for our results. In addition, we are also able to provide informative priors to encode expert knowledge into the system. In our example, our main source of prior knowledge is that the distribution is very likely Gumbel ($\xi$ is zero), which allows our model to converge on a solution faster.

The end-to-end investigation is available in the Pluto notebook provided, and an HTLM copy is available at https://patrickm663.github.io/extremevaluetheory/.

## Motivation
This repo was largely to showcase how `Turing.jl` can be used as a very flexible modelling library, given the support contraints when $\xi$ fluxuates around zero.

In addition, there has been little attention given to EVT in Julia.

## TODO
- [ ] Add example of Generalised Pareto Distribution
- [ ] Demonstrate how Bayesian neural networks can help model rare events by utilising block maxima / peaks-over-threshold to model the tails.
