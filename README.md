The project involved simulating an electromagnetic shower initiated by a single photon, investigating its dependence on the angle of incidence.

The shower develops at an altitude of 20 km, while the detector is located 4 km above ground level.

The study uses a parameter called the mean free path (radiation length) X0, which also serves as the unit of measurement for radiative energy loss. At a depth x, the residual energy is given by E(x)=exp[-x/X0], where the value used in this case is X0=7×10^4 cm.

The particles involved, electrons and positrons, are charged and therefore lose energy through ionization, which is the dominant process. On a large scale, this phenomenon appears continuous.

For photons, the dominant process is electron-positron pair production, with a mean free path equal to 9X0/7.

Expressing the path length in units of radiation length, t=x/X0, the number of particles is given by n=2^t. Given the initial energy E_0 of the incident particles, the energy of each particle is E(t)=E_0/2^t. The shower reaches its maximum when E(t)=E_C.

Therefore, at the shower maximum, the corresponding depth t_max is given by:

t_max=ln(E_0/E_C)/ln2.

To model this phenomenon, the Rossi model is used.

Each interaction occurs after a certain interaction length, and each secondary particle inherits half of its parent particle's energy. More specifically, at the level of individual particles, an electron or positron with energy E produces a photon and an electron or positron, while a photon with energy E produces an electron-positron pair.

The process stops when the energy of the electrons falls below the critical energy E_c, defined as the energy at which ionization losses become equal to radiative losses.

The user can choose the initial energy, ranging from 1 to 100 TeV, and the depth step "s", which can take values between zero and one, inclusive. A statistical study is also performed, for which the user specifies the number of events to simulate.

The program returns the profiles of three showers at incidence angles of 0, 20, and 40 degrees, respectively.

The statistical analysis produces a histogram showing the hit density as a function of the number of hits for the three incidence angles. A log-normal fit is also performed to investigate the distribution, since the phenomenon is stochastic.

The log-normal fit returns two parameters, \mu and \sigma. The first represents the mean of the distribution of ln(N), while the second represents the standard deviation of ln(N). These parameters describe the average behavior and fluctuations of the shower, respectively.

The histogram and the fit are plotted using logarithmic axes and logarithmically spaced bins, allowing the behavior of the showers to be characterized more effectively.

Another study investigates the relationship between the mean number of hits and the initial energy, for the depth step s specified by the user. The data are fitted with a straight line, and the parameter \alpha of the fit quantifies how linearly the number of hits increases with energy.

This plot is strongly dependent on the chosen depth step. For values of s up to approximately 0.4, the results agree with the physical model. Beyond this value, discrepancies begin to appear.

The final plot shows how the ratio \sigma/\mu, corresponding to the ratio between the standard deviation and the mean of the distribution, varies with energy for the depth step s selected by the user.

This result is also strongly dependent on the chosen step. Up to approximately s=0.4, the expected behavior is preserved: the ratio decreases as the energy increases.

The dependence of the last two plots on the depth step is explained by the fact that s determines how continuously the process is treated. If the process is discretized too coarsely, the simulation loses physical meaning and no longer produces realistic results. Examples of this include a ratio \sigma/\mu that increases with energy or a power-law fit that deviates from the expected behavior.
