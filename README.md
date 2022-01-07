# bayesian_opt_bug
For allowing others to reproduce bug we experience when running Bayesian Optimisation on Baumgartner_C-N data with Summit (built on BOTorch)

Question:
- Why do I get 'NotPSDError' when running MTBO with 50 datapoints?
- Surprisingly, it was able to complete 1 run of MTBO, NotPSDError was only raised on the second MTBO run. Furthermore, MTBO with 10 pretrainig datapoints was able to run 10 times, but it failed with 50 pretraining datapoints.
- 'NotPSDError: Matrix not positive definite after repeatedly adding jitter up to 1.0e-04.' Makes me think that two rows in the matrix of data are equivalent, however, why would the BO model query a point that it already has data for?

Data from this paper: https://pubs.rsc.org/en/content/articlelanding/2018/RE/C8RE00032H#!divAbstract
