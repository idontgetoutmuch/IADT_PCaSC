Code Readme

1.  **Sensitivity Analysis**

> i\. DriverBasic\_sens.m -- sens.mat and creates ranked sensitivities and
> time-varying sensitivities figures (Fig. S2A-B)

ii\. Covariance.m -- saves Correlations.mat

iii\. SensHeatmap.m -- creates heatmap figures (Fig. S2C-D)

2.  **Optimization**

<!-- -->

a.  [Individual Optimization]{.underline}

> i\. mainLogistic.m -- optimizes 4 parameters for each patient, saved into
> PARS\_4vary.mat

ii\. par\_boxplots.m -- creates parameter boxplots (Fig. S3A)

> iii\. ModelvData.m -- creates plot of model output versus data for all
> patients with 4 varying parameters (Fig. S3B)

b.  [Nested Optimization]{.underline}

> i\. NestedOpt.m -- nested optimization for training set, saves PARS.mat
> and rhovarphi.mat
>
> ii\. mainLogistic.m -- individual optimization for testing set patients
> using two uniform parameters in rhovarphi.mat
>
> iii\. PlotResults.m -- plots individual fit for training (Fig. S4A-B) and
> testing (Fig. 1A-B) patients. Also plots stem cell proportions (Fig. S5)
>
> ModelvData.m -- plots model output versus data for patients in
> training set (Fig. S4C) and testing set (Fig. 1C)
>
> iv\. par\_boxplots.m -- creates boxplots for ps and alpha for training
> (Fig. S4D) and testing (Fig. 1D) data sets
>
> v\. psvsalpha.m -- Fits a curve through ps versus alpha for training
> (Fig. S4D) and testing (Fig. 1D) data sets

c.  [Cycle by Cycle Optimization]{.underline}

> i\. CycbyCycOpt.m -- optimizes each cycle individually for each patient
> using two uniform parameters in rhovarphi.mat
>
> ii\. boxplot\_CyctoCyc.m -- plots boxplot of ps changes from cycle to
> cycle for training patients (Fig. 8A)

3.  **Forecast**

> i\. parCPD.m, parCPD\_2.m, parCPD\_3.m -- creates cumulative probability
> distributions of changes in ps from cycle to cycle (Fig. 8B)
>
> ii\. mainLogistic.m -- fits curves through ps versus alpha for each
> cycle, saves into psalphafit.mat
>
> ConfidenceInt.m -- plots ps versus alpha with fitted curve and 95%
> confidence interval (Fig. 8C)
>
> iii\. mainForecast.m -- forecasts response for each patient, given a
> cycle number and plots the results (Fig. 2)

4.  **Simulations**

<!-- -->

a.  [No Induction]{.underline}

> i\. NoInductionSims.m -- simulates IADT with and without induction, as
> well as continuous ADT. Saves time to progression (TTP) into TTP.mat and
> plots simulation results for each patient (Fig. 3G)
>
> ii\. SwimmerPlots.m -- creates swimmers plot comparing time on treatment
> for each patient (Fig. 3A-D)
>
> iii\. KapMeier.m -- plots Kaplan-Meier comparing TTP with and without
> induction and with continuous ADT (Fig. 3E)
>
> iv\. TTP\_Scatter.m -- compares TTP between each of the simulations for
> all patients (Fig. 3F)

b.  [Alternative Thresholds]{.underline}

> i\. ThresholdSims -- simulates IADT with alternative thresholds. Saves
> time to progression (TTP) into TTP.mat and plots simulation results for
> each patient (Fig. 4F)
>
> ii\. SwimmerPlots.m -- creates swimmers plot comparing time on treatment
> for each patient (Fig. 4A-C) for each threshold
>
> iii\. KapMeier.m -- plots Kaplan-Meier comparing Bruchovsky IADT protocol
> and alternative threshold IADT(Fig. 4D)
>
> iv\. TTP\_Scatter.m -- compares TTP between each of the simulations for
> all patients (Fig. 4E)

c.  [Induction Docetaxel]{.underline}

> i\. DOCSims.m -- simulates IADT with and without induction docetaxel for
> each patient (Fig. 5C-D)
>
> ii\. KapMeier.m -- plots Kaplan-Meier comparing TTP Bruchovsky IADT
> protocol IADT with induction docetaxel (Fig. 5A)
>
> iii\. PlotTTP.m -- compares TTP between IADT alone and IADT with
> induction docetaxel (Fig. 5B)

d.  [First Cycle Docetaxel]{.underline}

> i\. FirstCycDOCSims.m -- simulates IADT with and without docetaxel after
> first cycle. Saves TTP into TTP.mat and plots simulations results for
> each patient (Fig. 6D)
>
> ii\. boxplot\_BenvNoBen.m -- comparison of ps values between patients who
> do not benefit from docetaxel and those that do (Fig. 6A)
>
> iii\. KapMeier.m -- plots Kaplan-Meier comparing IADT with and without
> docetaxel after the first cycle. Stratifies based on ps value (Fig. 6B)
>
> iv\. TTP\_Scatter.m -- compares TTP between each of the simulations for
> all patients (Fig. 6C)

5.  **Leave-One Out**

<!-- -->

a.  [Leave-One Out]{.underline}

    i\. RunAll.m -- runs leave-one out study for each patient individually

b.  [ROC Analysis]{.underline}

> i\. ROC.m -- plots ROC curves for all patients simultaneously (individual
> ROC results saved in ROC.mat)
