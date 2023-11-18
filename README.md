# Polytomous-IRT-Analysis
Polytomous IRT Analysis using SAS
data mydata;
  set ABU.PJ4S5;
  array items(*) hwa134-hwa138; /* List all your items here */
run;

/* Fit the GPCM model for hwa134 */
proc itemresponse data=mydata;
  model hwa134 / grm; /* You can change "grm" to "gpcm" for Generalized Partial Credit Model */
  title 'Generalized Partial Credit Model for hwa134'; /* Change the title accordingly */
run;

