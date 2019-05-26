These calculations were made with a few different intial condition models and based on a few different papers so please be careful to make sure to cite the papers correctly when using these results.  The papers where the calculations were made are shown first and then below that you will find the model setup, assumptions, parameters, and appropriate papers to cite for each component of the model.


AuAu 200GeV  (eta/s=0.5, tau0=0.6 fm, TFO=150 MeV and TFO=165 MeV, and zeta/s=0)
	Trento Alba et al, Phys.Rev. C98 (2018) no.3, 034909
	mckln Not yet published, cite Noronha-Hostler et al, Phys.Rev. C93 (2016) no.2, 024909
PbPb 2.76 TeV (eta/s=0.47, tau0=0.6 fm, TFO=150 MeV, and zeta/s=0)
	Trento Not yet published, cite Alba et al, Phys.Rev. C98 (2018) no.3, 034909 since same setup
	mckln Noronha-Hostler et al, Phys.Rev. C93 (2016) no.2, 024909 ; Noronha-Hostler et al,  Phys.Rev. C95 (2017) no.4, 044901 ;Gardim et al,  Phys.Rev. C97 (2018) no.6, 064919 
PbPb 5.02 TeV (eta/s=0.47, tau0=0.6 fm, TFO=150 MeV and TFO=165 MeV , and zeta/s=0)
	Trento Alba et al, Phys.Rev. C98 (2018) no.3, 034909 ; Noronha-Hostler and Ratti arXiv:1804.10661 
	mckln Noronha-Hostler et al,  Phys.Rev. C95 (2017) no.4, 044901
XeXe 5.44 TeV (eta/s=0.47, tau0=0.6 fm, TFO=150 MeV and TFO=165 MeV , and zeta/s=0)
	Trento Giacalone et al, Phys.Rev. C97 (2018) no.3, 034904  ; Noronha-Hostler and Ratti arXiv:1804.10661
ArAr 5.85 TeV (eta/s=0.47, tau0=0.6 fm, TFO=150 MeV and TFO=165 MeV , and zeta/s=0)
	Trento Sievert and Noronha-Hostler  arXiv:1901.01319
OO 6.5 TeV (eta/s=0.47, tau0=0.6 fm, TFO=150 MeV and TFO=165 MeV , and zeta/s=0)
	Trento Sievert and Noronha-Hostler  arXiv:1901.01319 

These predictions were made using the Trento [1] initial condtions or [2] mckln initial conditions coupled to v-USPhydro [3] using the PDG16+/2+1[WB] Equation of State* [4] and the PDG16+ hadron resonance gas list [5].  

[1] TRENTO with "IP-Glasma" settings where p=0, k=1.6, and sigma=0.51: J. S. Moreland, J. E. Bernhard, and S. A. Bass, Phys. Rev. C92, 011901 (2015) 
[2] mckln
[3] J. Noronha-Hostler et al, Phys. Rev. C88, 044916 (2013); Phys. Rev. C90, 034907 (2014)
[4] S. Borsanyi et al., Phys. Lett. B730, 99 (2014); Alba et al, Phys.Rev. C98 (2018) no.3, 034909 
[5] Alba et al, Phys.Rev. D96 (2017) no.3, 034517


*When other equations of state are provide (e.g. PbPb and XeXe) then:

PDG05/S95n-v1 from Huovinen and Petreczky Nucl.Phys. A837 (2010) 26-53   eta/s=0.02, tau0=0.4 fm, TFO=145 MeV
PDG16+/2+1[WB] from S. Borsanyi et al., Phys. Lett. B730, 99 (2014)     eta/s=0.47, tau0=0.6 fm, TFO=150 MeV
PDG16+/2+1+1[WB] from S. Borsanyi et al., Nature 539, 69 (2016)       eta/s=0.47, tau0=0.6 fm, TFO=150 MeV

	
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%


Differential flow observables:

- The format is SPobs_CENsbvnc.dat where SP=species, obs=observable (e.g. avg, rn etc), CEN=centrality where 2=0-5%, 7=5-10%, 5=0-10%, and the rest are in 10% centrality bins with the number in the middle (e.g. 15=10-20%).  All calculations are done with the scalar product unless noted below.

-SPavg_CENsbvnc.dat contains:

	pT dN/dydpT v1(pT) psi1(PT) ... v6(pT) psi6(pT)

-SPcum_CENsbvnc.dat contains the differential cumulants (NOT scalar product):

	pT v1{2}(pT) v1{4}(pT) ... v6{2}(pT) v16{4}(pT) 
	
-SPscm_CENsbvnc.dat contains the differential symmetric cumulants (NOT scalar product):

	pT sc(3,2)(pT) sc(34,2)(pT) sc(4,3)(pT)
	
-SPrn_CENsbvnc.dat contains the factorization breaking:

	r2
	pT
	.
	. rn
	. rn rn
	r3
	pT
	.
	. rn
	. rn rn
	r4
	pT
	.
	. rn
	. rn rn
	where the values from left to right indicate biggest difference in pT <-> smallest difference in pT
	
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%
%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%%

Integrated flow harmonic observables: 

-All statistical error bars were generated using jackknife resampling.  

-Please ignore v1 results at this time.   

-Certain events are always removed from the calculations if integrated v_n<0 or v_n>0.25, if the multiplicity is 0 or shows large deviations.  Note that some events glitches while running in the int_X_pt0.2-3.dat files so they are set to all 0's.

The following files are included in each individual folder. The calculations are done using all charged particles:

	---------------------------

vn2err.dat*

Contains v_n{2} for v1-v6 in the order
	centrality v1{2} v1{2}_error v2{2} v2{2}_error ... v6{2} v6{2}_error
	
	---------------------------

vns1bin5.dat*

Contains v_n{4}^4 and v_n{6}^6 for v1-v6 in 5% bins in the order: 
	centrality v1{4}^4 v1{4}^4_error v2{4}^4 v2{4}^4_error ... v6{4}^4 v6{4}^4_error v1{6}^6 v1{6}^6_error v2{6}^6 v2{6}^6_error ... v6{6}^6 v6{6}^6_error
	
		---------------------------

vns1.dat*

Contains v_n{4}/v_n{2} and v_n{6}/v_n{4} for v1-v6 in 5% bins: 
	centrality v_1{4}/v_1{2} err ... v_6{4}/v_6{2} err  v_1{6}/v_1{4} err ... v_6{6}/v_6{4} err
	
		
		---------------------------

vns1bin.dat*

Contains v_n{4}^4, v_n{6}^6, and v2{2}/v_3{2} for v1-v6 in 1% bins: 
	centrality v_1{4} err ... v_6{4} err  v_1{6} err ... v_6{6} err  v2{2}/v3{2} err

	---------------------------
	
eccs.dat*

Contains calculations from the corresponding eccentricities for ecc_n{4}/ecc_n{2} and ecc_n{6}/ecc_n{4}* are shown in eccs.dat in 5% centrality bins where
	centrality ecc2{4}/ecc2{2} ecc2{4}/ecc2{2}_error ecc3{4}/ecc3{2} ecc3{4}/ecc3{2}_error ecc2{6}/ecc2{4} ecc2{6}/ecc2{4}_error ecc3{6}/ecc3{4}_error
	
	---------------------------
		
eccs1bin.dat*

Contains calculations from the corresponding eccentricities for ecc_n{4}/ecc_n{2} and ecc_n{6}/ecc_n{4}* are shown in eccs.dat in 1% centrality bins where
	centrality ecc2{4}/ecc2{2} ecc2{4}/ecc2{2}_error ecc3{4}/ecc3{2} ecc3{4}/ecc3{2}_error ecc2{6}/ecc2{4} ecc2{6}/ecc2{4}_error ecc3{6}/ecc3{4}_error
	
	---------------------------
	
eccs1bin.dat

Contains calculations from the corresponding eccentricities for ecc_n{4}/ecc_n{2} and ecc_n{6}/ecc_n{4}* are shown in eccs.dat where
	centrality ecc2{4}/ecc2{2} ecc2{4}/ecc2{2}_error ecc3{4}/ecc3{2} ecc3{4}/ecc3{2}_error ecc2{6}/ecc2{4} ecc2{6}/ecc2{4}_error ecc3{6}/ecc3{4}_error
	
	---------------------------
	
EPXXX.dat**

Contains event plane correlations with bin sizes of XXX (ask for details because depends on observable these are defined as in STAR's Npart^2*C_{n,m,n+m}*10^3)
	Npart ep224   ep224_err  ep235   ep235_err   ep246  ep246_err  ep336   ep336_err   ep112  ep112_err   ep123  ep123_err
	
	---------------------------	
	
EPXXXcomb.dat**

Contains event plane correlations with XXX harmonics (ask for details because depends on observable), NOT normalized
	centrality EPXXX EPXXX_err
	
	---------------------------
	
EPXXXratcomb.dat**

Contains event plane correlations with XXX harmonics (ask for details because depends on observable), normalized
	centrality EPXXX EPXXX_err
	
	---------------------------
	
SCMXXcomb.dat**

Contains symmetric cumulants with XX harmonics , NOT normalized
	centrality scXX scXX_err
	
	---------------------------
	
SCMXXratcomb.dat**

Contains symmetric cumulants with XX harmonic, normalized
	centrality scXX scXX_err
	
	---------------------------
	
	
Qs.dat

Contains linear Pearson Coefficients of ecc2-ecc4-> v2-v4
	centrality Q1*** Q1_err*** Q2 Q2_err Q3 Q3_err Q4 Q4_err
	
	---------------------------
	

	
Note that due to the limited number of statistics some centralities give imaginary results i.e. nan when higher statistics/finer centrality bins might avoid this. 

	

* At this point in time, centrality rebinning and multiplicity weighing are not included in these calculations but they may have small effects on the order of a few percentage points for central and peripheral collisions.  

** Centrality binning and multiplicity reweighing ARE considered here. 

*** ignore for now	
