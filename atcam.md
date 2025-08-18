---
layout: page
title: Project
use-site-title: true
---

*“Cosmological simulations opening a window to the initial conditions of the Universe” (CNS2024-154242)*

The origin of the initial conditions of the Universe are unknown. The structures that we observe today in the Universe grew from some initial perturbations
set during a very short period of time in the early Universe. Inflation is the most plausible description of an early and short period of cosmic time
experiencing the needed accelerated expansion. Many multi-field inflationary models predict non-Gaussian perturbations in the initial conditions of the
Universe's density distribution, the Primordial Non-Gaussianities (PNG).

Studying the effect that PNG have on the distribution of observables at later times, is one of the few ways to disfavour different inflationary models. The
level of local PNG can be quantified by the parameter f_NL. Cosmological surveys, such as DESI and Euclid, are aiming to study the imprints of the
epoch of inflation by measuring f_NL. These surveys are making accurate maps of cosmological tracers such as galaxies, QSOs and gas.

We cannot measure f_NL directly, but rather the product f_NL*bphi, with bphi being a parameter that depends on the cosmological tracer. Assuming a
known bphi, current cosmological surveys are expected to improve the precision on f_NL by a factor of 5. However, this will only be possible if we can
establish realistic priors on bphi.

We need to measure bphi in model catalogues to inform current cosmological surveys, so we can actually understand the initial conditions of the
Universe. This can only be done using catalogues generated with models that encapsulate the rich variety of physical processes relevant for the
evolution of cosmological tracers. DESI started taking data in 2020 and Euclid has been recently launched; the methods to measure the imprint of PNG
on the distribution of their cosmic tracers have not yet been validated.

Time is of essence to provide priors on bphi for different cosmological tracers, that are useful for cosmological surveys planning to constrain fnl, such as
DESI and Euclid.

With this project we will be able to use 3 methods to populate dark matter only simulations with cosmological tracers. In particular, with those types of
galaxies and QSOs targetted by current cosmological surveys such as Euclid and DESI. The galaxy models have free parameters that will be chosen
against observed data. We will develop an iterative emulator based on Gaussian processes to find the best fit parameters. We will measure bphi and p
for DESI and Euclid spectroscopic cosmological tracers. This will be done building upon a validated method for dark matter haloes.

The measurements of bphi derived from this project will allow to provide priors, facilitating a realistic interpretation of observations from cosmological
surveys. This will achieve an error on f_NL enough to disfavour a large set of inflationary models. This study has the potential to increase the robustness
in the measurement of f_NL by a factor of 5.

This project will provide priors on bphi for cosmological multi-tracers from catalogues produced with both physically motivated and
approximated models in simulations with PNG at different resolutions.


## The team

| <img src="./img/miguel.png" alt="Miguel" width="300"/>  | Miguel Icaza Lizaola did his PhD in Durham, UK, and then moved to KASI, South Korea. He is an expert in applying maching learning to large scale structure cosmology.|
| <img src="./img/adrian.png" alt="Adrián" width="300"/>  | Adrián Gutiérrez Adame is a teacher assistant at the Universidad Autónoma de Madrid while he developes his PhD in our group. He obtained his Physics degree and  Master in Theoretical physics in 2021 at the Universidad Autónoma de Madrid. He his working on developing [new numerical simulations](https://ui.adsabs.harvard.edu/abs/2022arXiv220411103A/abstract) to study primordial non-gaussianity fluctuations.|
| <img src="./img/joaquin.png" alt="Joaquín" width="300"/>  | Joaquín Delgado Amar obtained his Physics degree at the Universidad Autónoma de Madrid and he is currently finishing his master degree in Theoretical Physics. |


## Previous projects as IP
####“Illuminating the dark sector of the Universe”
ATCAM projects: 2019-T1/TIC-12702 and 2023-5A/TIC-28943

This project aimed to understand the dark sector of the Universe studying the galaxies that trace it. This sector constitutes over 95% of the total energy-matter content of the Universe. Its nature remains unknown, despite decades of continuous effort. In the next years cosmological galaxy surveys will focus on the characterisation of the dark sector of the Universe. This observational characterisation relies on having an improved understanding of galaxies as cosmological tracers. We urgently need to answer the following questions:

* How can theoretical models aid and support the interpretation of cosmological observations?
* How do galaxies trace the dark sector?
* How affected are cosmological probes by galaxy formation?
* How do galaxies trace the dark sector when different cosmologies (the global composition of the Universe) are assumed?

Answering these questions will get us closer to understanding the nature of our Universe. The theoretical development from this project will support the success of space missions, such as Euclid (to be launch in 2021), and ground telescopes, such as the LSST (to start operating in 2023). Investments of millions of euros have been made in these and other ones, such eBOSS, DESI, WFIRST, etc.

The publications related to this project can be read [here](https://ui.adsabs.harvard.edu/search/q=docs(library%2FYgun0COhQQe8MdUjeP9mlw)&sort=date%20desc%2C%20bibcode%20desc&p_=0).

You can listen to a talk with an overview of the progress done so far [here](https://www.youtube.com/watch?v=afiQe9KN9k8).

## Previous team members

| <img src="img/sujatha.png" alt="Sujatha" width="300"/> |Sujatha Ramakrishnan is a post-doctoral researcher exploring how to use dark matter haloes beyond the resolution of numerical simulations. She did her PhD under the supervision of Aseem Paranjape, at the Inter-University Center for Astronomy and Astrophysics, Pune, India. Her thesis topic was the quantification of the environment of dark matter haloes.|
| <img src="img/Bernhard_Vos.png" alt="Bernhard" width="300"/> | Bernhard Vos Ginés obtained his degree in Physics at the Universidad de La Laguna in 2019 and his Master in Theoretical physics in 2020 at the Universidad Autónoma de Madrid. During his Master he obtained a JAE Grant for 9 months supervised by Santiago Ávila, in which he investigated Large Scale Structure topics as Baryonic Acoustic Oscillations using gas. Currently he is working on topics related with computational cosmology, generating galaxy mocks adapted to eBOSS and DESI surveys using Halo Occupation Distribution models. He is part of the DESI collaboration.|
| <img src="img/guillermo.png" alt="Guillermo" width="300"/>  | Guillermo Reyes Peraza is developing his PhD thesis. He obtained his Physics degree at the Universidad de La Laguna in 2018 and his Master in Theoretical physics in 2019 at the Universidad Autónoma de Madrid. He his working on better understanding galaxies with spectral emission lines using a semi-analytical model of galaxy formation and evolution, [SAGE](https://ui.adsabs.harvard.edu/abs/2022MNRAS.510.5392K/abstract). This is in preparation to the ESA satellite [Euclid](https://sci.esa.int/web/euclid), in order to be able to develop fast galaxy catalogues.|
| <img src="img/julen.png" alt="Julen" width="300"/> |Julen Expósito is hired for a year within the program ["Yo Investigo"](https://sede.comunidad.madrid/ayudas-becas-subvenciones/programa-investigo) from Comunidad de Madrid. He is further developing the publicly available code [get_nebular_emission](https://github.com/galform/get_nebular_emission) for modelling spectral emission from both star forming and AGN regions. He did his masters at the Intituto Astrofísico de Canarias.|
| <img src="img/marco.png" alt="Marco" width="300"/> |Marco Molina exploring Halo Occupation Distribution models for [DESI](https://www.desi.lbl.gov/) QSOs for his master thesis at the Universidad Autónoma de Madrid, where he also studied his undergraduated degree.|
| ![Santi](img/santi.png =x300) |  Santiago Avila is a postdoctoral researcher working in the field of Large Scale-Structure (LSS) from both the computational and an observational point of view. His main interests are Baryonic Acoustic Oscillations (BAO), Primordial Non-Gaussianities (PNG), the impact on galaxy clustering of the connection between galaxies and dark matter and fast cosmological simulations. He is co-convener of the Dark Energy Survey LSS science working group, in charge of BAO analysis and galaxy clustering for combination with Weak Lensing. He is also an active member of Euclid, DESI and SKA, he was also member of eBOSS in the past. Currently, he is also working on creating and analysing a unique suite of simulations to understand the effect of PNG on galaxy clustering. Santiago is also very active in outreach and public communication. |
| <img src="img/angel.png" alt="Ángel" width="300"/> |Ángel Chandro studied both his Physics degree and master at the Universidad Autónoma de Madrid. He started working in the group during the summer of 2021 with a summer project and then he continued to develop his master thesis supported with a grant. He has been working on the infrastructure to be able to run semi-analytical models of galacy formation and evolution, [SHARK](https://github.com/ICRAR/shark) and [GALFORM](https://ui.adsabs.harvard.edu/abs/2020MNRAS.498.1852G/abstract), on the dark matter only simulation [UNITSIM](https://ui.adsabs.harvard.edu/abs/2019MNRAS.487...48C/abstract)|
| ![Olivia](img/olivia.png =x300) | Olivia Vidal finished her Physics degree in 2022 at the Universidad Autónoma de Madrid. She developed, with a short contract, a big part of the public code [get_nebular_emission](https://github.com/galform/get_nebular_emission), This is a modular code to produce model spectral emission lines for a given input of stellar mass, metallicity and star formation rate. |
