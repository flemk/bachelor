# ECG time series and stochstic analysis

## The Idea
Estimation of Kramers-Moyal-coefficients from ECG heart data gives us a stochastic model of the heart. This can be used to reconstruct time series.

## The procedure
- Analysis of each signal using Karhunen-Loev method: 
$$
\dot{x}=v \\
\dot{v}=f(x,v)
$$

- Is there some interplay between electrodes?

    $$
    \frac{\partial D_v^{(1)}}{\partial t} \text{ fit nach } f(x_1, v_1, x_2, v_2, ..., x_n, v_n)
    $$

    This is so the Kramers-Moyal-coefficients estimation.
    
    Derivation of coupling coefficients -> How great is the coupling between electrodes?

- From step one we retrieve a 14D ODE system

- Fokker Planck analysis of the system(s)

## Literature so far
- J.Gradisek, S.Siegert, R.Friedrich, I.Grabec: Analysis of time series from stochastic processes, Physical review E, Sep 2000
    
    This is the method to estimate Kramers-Moyal coefficients

- O.Kamps, J.Peinke: Analysis of noisy spatio-temporal data, Understanding complex systems, Springer 20016 [Das war diese Konferenz]

    A extension of a method to extract Langevin equations from noisy spatio-temporal data. Mainly this paper lead us to the others. It itself was rather unhelpful.

- T.Kuusela: Stochastic heart-rate model can reveal pathologic cardiac dynamics, Physical review E 69, 2004

    This is an example of the application of Kramers-Moyal coefficient estimation. He uses RR-Intervals (very elegant!), while we use the raw data.

- C.Honisch, R.Friedrich: Estimation of Kramers-Moyal coefficients at low sampling rates, ?, Oct 2018

    If the time series is present only in low sampling rates the result of the KM estimation can be improved by solving a adjoint FPE and optimize a term (18).

- F.Böttcher, J.Peinke, D.Kleinhans, R.Friedrich, P.Lind, M.Haase: Reconstruction of complex dynamical systems affected by strong measurement noise, Physical review letters 97, Sep 2006

    When the time series data is subject to stron measurement noise the KM estimation results can be improved optimizing term (10).