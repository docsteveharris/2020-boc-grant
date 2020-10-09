Hi Harry. Excuse the double pronged text and email attack. Am writing a 4-year fellowship grant app at short notice (deadline 31 Jan). Not a lot of £ but good opportunity and only comes round every 4 years. I'd like to base this at IHI and would need your support. Did you have 30mins to discuss? 

Dear Harry

Excuse the double pronged text and email attack. Am writing a 4-year fellowship grant app at short notice (deadline 31 Jan). Not a lot of £ but good opportunity and only comes round every 4 years. I'd like to base this at IHI and would need your support. Did you have 30mins to discuss? 

Background in brief:
- British Oxygen Company (BOC) Chair of Anaesthesia Fund ... endowment of a research fellowship in a department of Anaesthesia.   to support ... working towards a senior fellowship or developing a credible application for a Chair in Anaesthesia (or related specialties) in the next five years. Applications are welcomed from clinicians and from basic scientists with a similar ambition. See https://www.niaa.org.uk/article.php?newsid=1474
- **£80k/year for 4 years**; reasonably flexible spend and charitable so I assume this can be leveraged by UCL if I'm successful
- I'd like to bring together 3 themes
	- IHI/you/CRIU and adaptive embedded trial design
	- [Ramani Moonesinghe](https://www.ucl.ac.uk/anaesthesia/people/professor-ramani-moonesinghe-frca-mrcp-fficm-mdres) who is friend and collaborator; we've previously worked together on a national trial and this would clearly orient the work to the anaesthesia/periop domain
	- Critical Care Health Informatics Collaborative (with Merv) 


Proposal in brief:
- Leverage CC-HIC and add a 'peri-op' arm
	- **expand to all inpatient surgery**; equivalent to approx 4000 cases per trust per year (1 million cases per year across the NHS); difficult to do this beyond UCLH with this budget but would aim to find additional money to scale
	- **leverage existing snap national audit experience**, data and design (SNAP-2: Moonesinghe, SR, DJN Wong, L Farmer, R Shawyer, PS Myles, **SK Harris**, ‘SNAP-2 EPICCS: the second Sprint National Anaesthesia Project-EPIdemiology of Critical Care after Surgery: protocol for an international observational cohort study.’, BMJ Open vol. 7, no. 9, 2017, pp. e017690.)
	- argue that this creates the framework for a unique scalable international resource for studying surgical outcomes
- Iterate on the REMAP methodology (Randomised Embedded Multi-factorial Adaptive Platform Trials; Angus, DC, ‘Fusing Randomized Trials With Big Data: The Key to Self-learning Health Care Systems’, JAMA vol. 314, no. 8, 2015, pp. 767-768.) but for 'small beans/marginal gains' stuff with a heavy emphasis on using EHR phenome to investigate and exploit treatment heterogeneity 
	- select routine treatments decisions with significant variabilty and clinical equipoise
	- embedded nudged rather than mandated randomisation
		- where clinician complies with nudge then use instrumental variable analysis to get at the causal effect
		- where the clinicians refuse to comply then define the phenome of the subgroup

Worked example: paracetamol for post-operative fever
- paracetamol pros: pain/comfort
- paracetamol cons: masks fever and delays recognition of infection; blunts immune benefits of hyperthermia
- demonstrate that there is variation in practice
- then embed a nudge in the EHR to prescribe/not prescribe post-operatively
- follow-up process measures
	- patient characteristics (e.g. are we more nervous about harm from fever in patients who have neurosurgery)
	- antibiotic prescribing patterns
	- postive microbiology in the early post-operative period
	- patient length of stay 
- follow-up longer term outcome measures including survival


Worked example: oxygen prescriptions post-operatively
- oxygen pros: tissue oxygenation; wound healing
- oxygen cons: lung injury; altered cell differentiation in healing etc
- demonstrate that there is variation in practice
- then embed a nudge in the EHR for high/low SpO2 targets
- follow-up process measures
	- patient characteristics (e.g. are we more nervous about harm from O2 in patients who COPD)
	- respiratory complications (use POMS)
	- patient length of stay 
- follow-up longer term outcome measures including survival

Proposal in 3 lines:
1. Leverage CC-HIC and add a 'peri-op' arm
	- existing data sharing agreements and data management toolkit
	- add in inpatient surgery initially at UCLH but with the governance to scale to other CCHIC sites
2. Pilot REMAP-Nudge. That is embed a randomised trial into the EHR at UCLH that focuses on developing personalised treatment strategies for routine care (marginal gains). Every treatment decision is either 
	- 'nudged' toward best practice where there is clear evidence
	- randomly 'nudged' so that it becomes an 'n of 1' learning event that quickly scales because we embed the nudge in the EHR and use a presumed consent/opt-out model

