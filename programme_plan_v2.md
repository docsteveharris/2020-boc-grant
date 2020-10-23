Over 4 years
we are building the infrastructure for interventional platform trials in critical care

- [ ] TODO run a parallel approach of nudge and non-nudge; that is can you implement a lightweight 'results' only RCT that tackles the same cpap question but without the nudge component; that is can you offer some certainty to the grant panel that you'll achieve something; saying this out loud makes me think that's the wrong target; others should take on the RCT piece; what you'll provide is the groundwork for the RCT (prove equipoise/variation/identify boundaries for qns etc.)

choose a high risk and a low risk target question
cpap=high
oxygen targets = low

WP1
Data in
Build a respiratory support component to CCHIC
This will be the basis of the network that you're going to use to implement the trial
Will involve benchmarking and data quality control
Deliverables
Regular early respiratory support updates on COVID in details as per DECOVID
- think of this as the ISARIC for respiratory support
- basis of a platform for trials
Modification to include inpatients regardless of location ('critical care without walls')

## Work package 1: CCHIC-COVID
**Deliverable: an extension to the Critical Care Health Informatics Collaborative (CCHIC) that focuses on respiratory failure in COVID-19**

The NIHR established the Health Informatics Collaborative in 2014. UCL/UCLH has led the Critical Care theme.[@harris2018b] I have co-led the project (with Singer/Brealey/MacCallum) since 2015. We have ethics (REC 14/LO/103) and CAG approval (14/CAG/1001) plus data sharing agreements for 7 UK sites (including Cambridge/GSTT-Kings/Imperial/Oxford/UCL and now the Royal Marsden and Bristol). Routinely collected clinical data from critical care admissions is transferred to UCL's  ISO/IEC 27001:2013 compliant [data safe haven](https://www.ucl.ac.uk/isd/services/file-storage-sharing/data-safe-haven-dsh) where it is organised, cleaned, linked to Hospital Episode Statistics ([HES](https://digital.nhs.uk/data-and-information/data-tools-and-services/data-services/hospital-episode-statistics)) to define health care utilisation and long term survival, and then made available as resource back to the critical care community.
Since 2015, **we have curated data for >45,000 admissions to critical care with 250 data items and >250 million data points**. This resource has led to a series of publications[@palmer2019a; @meiring2018], and high profile presentations (Hot Topics, Intensive Care Society 2019). We have also launched an educational programme including datathons and training courses for clincal data scientists.[@harris] We have had a favourable review of our ethics (2019 5 year review), and ongoing support at PPI events.

We will now:

1. **Seek extensions to the research governance we currently hold to process identifiable data for all inpatients with COVID-19 at risk of critical illness**
We are currently in the process of applying for an extension to the ethics approval for CCHIC that will allow us to follow all inpatients admitted to the hospital with COVID-19 as their primary reason for admission. We are confident that this time limited extension to our governance will be granted on the grounds of the existing guidance ([Covid-19 – Notice under Regulation 3(4) of the Health Service Control of Patient Information Regulations 2002](https://www.gov.uk/government/publications/coronavirus-covid-19-notification-of-data-controllers-to-share-information/coronavirus-covid-19-notice-under-regulation-34-of-the-health-service-control-of-patient-information-regulations-2002-general)). 

2. **We will expand the data specification to include key case mix measures for respiratory failure**.
We currently hold sufficient information to define severity of illness and the major organ failure components. We do _not_ hold detailed information on mode of ventilation, on medical interventions to support respiratory failure (e.g. bronchodilators, mucolytics etc.), on mechanical interventions (e.g. secretion clearance, humidification techniques), on rescue therapies for respiratory failure (e.g. prone positioning, nitric oxide, ECMO referral etc.) nor do we hold information on COVID-19 specific therapies (e.g. anti-virals including remdesevir, vaccine history, convalescent plasma etc.). 

These complex data types have been the target of the initial modelling effort by the [DECOVID research programme](https://www.decovid.org) who are co-hosted between UCLH (the lead site for CCHIC) and University Hospitals Birmingham (UHB). This allow us to leverage this data modelling effort and rapidly deploy the same for CCHIC (via Co-Investigator Dr Wai-Keong Wong).

- [ ] TODO Bryan Williams : letter of support
- [ ] TODO CHIMERA collaboration?

3. **We will report on long term outcomes for COVID-19 pneumonia using data linkage from CCHIC to ONS**
The unique strengths of CCHIC is that we have the infrastructure to link to NHS-Digital and the Office of National Statistics. We will use this to capture in the first instance long term mortality. Existing resources such as ICNARC and DECOVID report hospital mortality only. We will also make available the data linkage to Hospital Episode Statistics such that long term health care resource utilisation can be studied.

4. **We will add metadata to all drugs, orders, and treatment decisions to capture a patterns of clinician behaviour**
We will also update the ethics arrangements for CCHIC to capture a pseudonymised identifier for the clinical decision maker. The identifier will be created using a one-way hash as want to protect the individual clinician from being re-identified yet reliably track their behaviour, approach and decisions.  We will label all drugs, orders, and treatment decisions with the clinician's identifier in preparation for the physician-prescribing preference studies (see WP3).[@rassen2009c] 



## Work package 2: Using variation in practice to identify priority areas for intervention
**Deliverable: A series of priority areas for interventional evaluation**

- [ ] TODO prepare proof that clinicians have local levels of doubt (you may need to do the PPP bit first) and then decide whether you think about the randomisation at the centre level or at the individual level
- [ ] TODO letter of support from Bryan et al
involve Reecha and Natalie Fitzpatrick and the AboutMe programmes

- [ ] TODO think about quality of care and improving that quality be working on the basics well (tidal volume, sedation etc. all the things that we have learned over the last 20-30 years of ICU)
- [ ] examine whether the variation in practice is associated with the variation in outcomes; model this behaviour; think of this explanatory variable at the unit level? compare to non-COVID respiratory failure work; this should be an analysis and an output too

We have prepared a worked example but it should be noted that in the actual project, the intervention to be tested will be developed and selected via a joint clinician/patient/public programme, and not investigator driven. This is especially important given that we will be moving to a presumed consent/assent model that we will depend on the clinical workforce to engage with the **nudge-learning** approach. Hence the actual question to be studied may vary. 


set up transition from CPAP to IMV here
do this with PPI
WP2
Data back with reports
Build a 'learning health care system' with regular reports and updates back to the centres
Think of this as ICNARC plus but focused on respiratory themes and capturing data from the sites that describes the longitudinal implementation of respiratory support
Look at a range of interventions that need assessing
- proning
- o2 targets
- timing of CPAP
Make these reports available to local teams but not invest more at this stage in QI methodology
Some ability to see if timely local reporting actually delivers improvements in and of itself

## Work package 3: Causal inference using physician-prescribing preference to identify target trials
Physician prescribing preference work on those targets
Define variation in practice
Specific ambition to look at timing of CPAP to IMV transition
Possibly consider other causal inference techniques such as regression discontinuity designs by capturing the local protocols and guidance from each centre

## Work package 4: Pilot nudge-learning trial
WP4
Pilot nudge implementation (high tech)
Define the targets that you need to capture the data

## Work package 5: Pilot nudge-learning trial
WP5 
Pilot nudge implementation (low tech): how could this be scaled; could it work in non digitally mature centres
NCL network
RECOVERY style reporting





