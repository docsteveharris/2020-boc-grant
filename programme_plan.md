---
title: Programme plan
export_on_save:
    pandoc: true
output: word_document
date: 2020-10-27
author: Steve Harris
bibliography: references.bib
# csl: plos-medicine.csl
csl: science-without-titles.csl
word_count_target: 5000
---

# Title

Precision Medicine via Embedded Decision Support with Randomisation (PreMEDS+R): Developing a novel trials methodology for peri-operative medicine

# Aim and objective (aka hypothesis)

> When there is genuine equipoise between two commonly used treatments, _not_ doing a point of care trial to find out which has a better risk/benefit profile seems _unethical_. Pragmatic RCTs could enable clinically important questions that can be answered fast based on studies carried out in routine care settings on a full range of participants.

**Learning Health Care Systems in the NHS**. Nuffield Trust Seminar, January 2019[@scobie2020]

## Hypothesis
That there is a portion of clinical care that can be optimised in a methodologically rigorous and ethically sound manner without resorting to standard parallel arm randomised controlled clinical trials.

## Aim
This project aims to develop the framework for a learning health care system for peri-operative medicine using established infrastructure at a single site but with a pathway to scale to multiple sites. 

### Deliverables (Work packages)
1. A high-quality prospective peri-operative medicine database built to scale across multiple NHS sites
2. A templated pipeline from question to study implementation that includes
	- evidence of variation in routine practice related to the bedside clinician
	- causal observational evidence of effect size using an physician prescribing preference design
	- statistical simulation procedures that allow estimates of sample size and treatment heterogeneity to permit triage of promising questions
	- decision support to reduce unwarranted variation
	- a randomisation tool that creates learning opportunities embedded in the electronic health record
	- patient and public engagement to support the design and expansion of the programme from a pre-emptive to an opt-out consent model
3. A pilot embedded randomised controlled trial using a novel _nudge_ design also built to scale across multiple NHS sites (**PreMEDS+R**).

I provide two worked examples below. However, this proposal is methodological, and other clinical questions would also be suitable, and may be prioritised by the integrated patient and public involvement (PPI) pathway.

Study exemplars:
- Comparison of conservative versus liberal oxygen targets on post-operative morbidity following high risk surgery admitted to critical care
- Comparison of high versus low targets of magnesium supplementation on post-operative atrial fibrillation following high risk surgery admitted to critical care	 


---

# Introduction
**Hundreds of millions of decisions** are made every day by doctors, nurses and allied health professionals. Most decisions are so small and routine that we don't always notice them: do we give paracetamol for a fever? do we target an oxygen saturation of 94% or 98%; do we stop the antibiotics this morning or this afternoon? But it is inconveivable that the aggregate effect of all these decisions is unimportant.
Randomised controlled trials (RCTs) are our 'go to' method for studying a single decision. But **traditional RCTs are slow, expensive and cumbersome**. Moreover they deliver results that are true on _average_ but not adapted for the individual. Personalised medicine recognises that variations in genotype and phenotype require treatments to be appropriately adapted. With unlimited sample size, such evidence could be generated but the cost would be prohibitive. Machine learning (ML) offers to use 'big data' to derive endotypes[^b] but without randomisation observational research remains vulnerable to bias through unmeasured confounding. This is also true for Artificial Intelligence (AI) techniques such as reinforcement learning.[@palmer2019; @komorowski2018]
Parallel two arm (A vs B) RCTs are now being replaced with intelligent designs such as REMAP (**Randomised Embedded Multifactorial Adaptive Platform**) trials.[@angus2015] This automates data collection by **E**mbedding the trial in electronic health record (EHR). It **A**dapts the randomisation algorithm so that as a signal for benefit or harm emerges patients are preferentially allocated to the best strategy. And finally, **M**ultiple treatments (factors) are evaluated together using the same **P**latform so the cost of setting the trial up is shared. REMAP-CAP is the first attempt at this approach evaluating antibiotics, anti-virals and steroids for Community Acquired Pneumonia (CAP).[@2016a] Nonetheless, this is still a hugely expensive international collaboration recruiting initally 2800 patients across 50 sites over several years.[@2016b]
The final result from REMAP-CAP will true _on average_ but cannot provide the right answer for the each patient who may have an allergy to the 'best' antibiotic, or be more susceptible to the immune suppression induced by the steroids, and so on. This **treatment heterogeneity** is driven by subtle endotypes not exposed by the RCT.[@iwashyna2015a] And herein lies the skill of the clinician. To take that average answer and decide if it applies to the particular situation. But while there is shared expertise, each clinician's personal experience creates variation. 
We normally see such variation as a problem.[@wennberg2011] Electronic Health Record Systems (EHRS) often provide clinical decision support tools to improve compliance with evidence and reduce variation. It is assumed that the busy clinician who is more often unwittingly deviating from a guideline rather than personalising treatment. 
But what if we used decision support to both **reduce variation where strong evidence is available, _and_ to learn from the existing variation where evidence is sparse**.
We call this approach _**nudge learning**_, and propose a trial design called _**PreMEDS+R**_. This design will ultimately depend on _presumed_ (opt-out) consent to allow the trial to scale, and through that scale investigate treatment heterogeneity. However, such a paradigm shift in clinical trial implementation requires a pragmatic and stepped approach. This project proposes a stepped implementation building first (1) a high quality database to confirm treatment variation and capture the rich data needed for an embedded RCT; then (2) a programme of work that carefully evaluates patient and clinician acceptance of a nudge methodology; and (3) implements a pilot PreMEDS+R trial in high risk surgery to estimate nudge compliance, and likely treatment effect sizes. The design is such that if successful the pilot study will then transform to a multi-site learning health care  programme to optimise care of the high risk surgical patient. 
We argue that this is the perfect domain in which to develop this methodology because **we leverage the anaesthetic pre-assessment clinic** to run the initial work using a _pre-emptive_ rather than presumed consent model.

# Background
**Learning health care systems** "... integrate the practice of medicine and the generation of reliable medical evidence in a way that will promote both continuous learning and evidence based medical practice.[@london2018] 

A learning health care system stops short of using RCTs as a methodology. Instead, they depend on cycles of observation and intervention: a version of quality improvement's Plan-Do-Study-Act (PDSA) cycle. The interventions are not novel experimental therapies but recommendations from existing practice supported by expert opinion, guidelines and consensus recommendations some but not all of which may be based on RCT evidence.  Typically a panel of performance indicators is devised and tracked. As each intervention is implemented, these indicators are used to evaluate its impact and justify modifications, adjustments or new interventions. Inevitably, these PDSA style cycles cannot meet the standards of objectivity that an RCT can offer. There are prone to the same types of bias observational research must overcome.

The programme of work proposed here integrates digital health and _nudged_ rather than _mandated_ randomised interventions to create a safe, ethical delivery framework for this oft-cited and yet rarely implemented goal. I specifically focus on optimising the delivery of routine health care where pre-existing variation in practice implies clinical equipoise. The end result would be a system that delivers causally robust personalised treatment effects at scale.

I build on the following three concepts: digital health, nudged interventions, and variation in practice:

1. **Digital health**

>  Digital health can potentially offer the solutions needed to transform clinical trials ... However, this cannot be accomplished by replicating the current research processes and just transforming them from paper to digital form ... Rather, a complete re-thinking and re-engineering of the clinical trial experience around the participant rather than the research site is needed.[@steinhubl2019]

2. **Nudged interventions**

> A nudge ... is any aspect of the choice architecture that alters people’s behavior in a predictable way without forbidding any options ... Nudges are not mandates.[@thaler2009@6]

3. **Variation in practice implies clinical equipoise and treatment heterogeneity** 	

- > equipoise[^a]: ... honest, professional disagreement among expert clinicians about the relative clinical merits of interventions A and B for a particular patient population[@london2018] 

- > treatment homogeneity versus heterogeneity[@longford1999]:
> - homogeneity: treatment B is superior to treatment A for (almost) everybody in the designated population; 
> - heterogeneity: treatment B is superior to treatment A for an average or typical subject in the designated population. *B may be inferior for a non-trivial proportion of subjects*.

Most importantly, it is crucial that this proposal is not read as a criticism of randomised controlled trials (RCT) in general. Rather this is an adaption of the RCT methodology to meet the need to deliver evidence based personalised medicine recommendations. As such, this approach is inappropriate for the investigation of novel drugs and interventions (e.g. CTIMPS, ATIMPS and other scenarios).

4. **Randomised controlled trials are not well adapted for non-binary questions**

A Phase 3 trial comparing a new drug to a placebo is well suited to an RCT. However many questions in medicine are non-binary, and the RCT implementation often loses subtlety.  
This in turn means clinicians lose equipoise. 
Consider, as an example, the ARDSNet study of high versus low tidal volume ventilation, arguably the most famous trial of in critical care.[Acute et al., 2000, #66550] This reported that mortality was lower for mechanically ventilated patients if the tidal volume was 6ml/kg rather than 12ml/kg. Critics have often pointed out that the tidal volumes in the 'high' group was excessive.[@laffey2000] But more fundamentally, the trial is structurally unable to define the 'optimum' tidal volume (even on average). For that, we would need a multi-arm trial with patients assigned tidal volume targets ranging from below 6ml/kg up to 12ml/kg (i.e. 4ml/kg, 5ml/kg, 6ml/kg, 7ml/kg ...). Forcing a binary choice has further consequences. The bedside clinicians will often find that the dichotomy is too stretched for his or her patient. In other words, they loose equipoise because one or more of the arms is too far from their own judgement (e.g. 6 versus 12 ml/kg). Without equipoise, the clinician cannot with conscience enrol the patient.
A similar critique can be made of strategies that evaluate antibiotic duration, fluid balance, the optimum blood pressure, oxygen targets, or the timing of interventions. All of these are decisions that rest on a 'fine balance' of clinical judgement. 

# Project plan

This 4 year programme will build on three existing programmes. 

1. The established **Critical Care Health Informatics Collaborative** (CCHIC) programme that holds data on 45000+ adminssions from 10+ NHS ICUs.[@harris2018b] The existing governance and data flows create an opportunity to magnify the influence of the RCOA/BOC grant to scale across multiple sites. 
2. The **Experimental Medicine Application Platform** (EMAP) at UCLH where I have a proven track record of deploying novel applications in realtime against the hospital wide EHRS. More specifically, my team has spent the last two years building EMAP exactly to enable this sort of work.  EHR systems alone do not permit innovation and development. They are hampered by vendor lock-in, and by the need to prioritise clinical safety and reliability above all else. EMAP is a data science platform built for the NHS inside the NHS according to the following principles (1) Protection of operational systems by deploying a live mirror of the EHRS (2) Protection of patient privacy by following a 'code-to-data' rather than 'data-to-code' paradigm (3) Health care interoperability to permit cross-site collaboration and (4) Open source to foster a community of practice.
3. An existing collaboration with the Centre for Peri-operative Medicine at (CPOM) that has nurtured the last two Sprint National Anaesthesia Projects (SNAP). Together with Professor Moonesinghe, I co-led SNAP-2 that built and managed an (inter)national data set for high risk inpatient surgery.

## Work package 1: CCHIC-Peri-op
**Objective: Build an extension to the Critical Care Health Informatics Collaborative (CCHIC)**

The NIHR established the Health Informatics Collaborative in 2014. UCL/UCLH has led the Critical Care theme.[@harris2018b] I have co-led the project (with Singer/Brealey/MacCallum) since 2015. We have ethics (REC 14/LO/103) and CAG approval (14/CAG/1001) plus data sharing agreements for 7 UK sites (including Cambridge/GSTT-Kings/Imperial/Oxford/UCL and now the Royal Marsden and Bristol). Routinely collected clinical data from critical care admissions is transferred to UCL's  ISO/IEC 27001:2013 compliant [data safe haven](https://www.ucl.ac.uk/isd/services/file-storage-sharing/data-safe-haven-dsh) where it is organised, cleaned, linked to Hospital Episode Statistics ([HES](https://digital.nhs.uk/data-and-information/data-tools-and-services/data-services/hospital-episode-statistics)) to define health care utilisation and long term survival, and then made available as resource back to the critical care community.
Since 2015, **we have curated data for >45,000 admissions to critical care with 250 data items and >250 million data points**. This resource has led to a series of publications[@palmer2019a; @meiring2018], and high profile presentations (Hot Topics, Intensive Care Society 2019). We have also launched an educational programme including datathons and training courses for clincal data scientists.[@harris] We have had a favourable review of our ethics (2019 5 year review), and ongoing support at PPI events.

- I will extend the scope of the ethics and the collaboration agreements with participating sites to the same cohort studied under the recent 2^nd^ Sprint National Anaesthesia Project (SNAP-2 EpiCCS: Epidemiology of Critical Care after Surgery).[@moonesinghe2017] That is **patients staying in hospital overnight undergoing a surgical or interventional procedure that requires the prescence of an anaesthetist**.
- I will expand the data specification to include **key case mix measures for peri-operative medicine** (patient comorbidites, risk factors, surgical procedures, anaesthetic techniques and intra- and post-operative complications) leveraging experience with SNAP-2, PQIP[@wagstaff2019] and NELA[@eugene2018]
- I will standardise and generate **five high quality outcome measures** from these data (1) mortality (2) length of stay (3) planned and unplanned critical care admission and (4) POMS[@grocott2007] and (5) using the existing CCHIC permissions (HES/ONS) to define health care utilisation and long term survival
- I will add metadata to all drugs, orders, and treatment decisions to capture a pseudonymised identifier for the clinical decision maker to build evidence for variation in practice, and preparatory physician-prescribing preference studies[@rassen2009c]
- the scale and scope of data collection requires hospitals that have integrated Electronic Health Records (EHRs). The interventional arm of the study further requires a working clinical decision support technology. I have already had a favourable response from approaching the Cambridge BRC (see attached letter of support from Dr Ari Ercole). 

We would see this CCHIC:Peri-op becoming the _premier international resource for observational studies of high risk surgery and peri-operative medicine_. Just at UCLH trust (including RNTNE, NHNN, WMS) I would expect to recruit >10,000 patients per year. Using the NIHR Health Informatics Collaborative network as a springboard alongside extensive and broad networks developed running SNAP-2/EpiCCS, I would seek funding to expand to further sites during the 4 years.

## Work package 2: PreMEDS+R trial incubator
**Objective: Build a pipeline for delivering such trials from question to implementation**


## Work package 2A+2B: A toolkit for Clinician Prescribing Preference studies
**Objective: Build a pipeline for rapid observational evaluation of variation in practice and evaluation of proposed interventions**

Clinician Prescribing Preference (CPP) studies exploit natural variation in practice. A classic example comes from the psychiatric literature where GPs have been show to have consistent preferences for different classes of Selective Serotonin Uptake Inhibitors (SSRIs) and Tricyclic Antidepressants (TCAs).[@davies2013] Patients treatments therefore depended on which GP they attended. Given that GP assignment can be argued to be unrelated to the self-harm/suicide (after controlling for social deprivation etc.) then this permits an evaluation of the relative effectiveness of these drugs.

My group has already completed an initial evaluation of this approach studying magnesium supplementation. We examined adult admissions to University College London Hospital Critical Care Unit (2016-17). Each patient’s admission was divided into ‘treatment windows’: including a serum magnesium measurement, an opportunity for supplementation linked to the bedside nurse on duty, and a period of observation (roughly equivalent to the 'day shift') for Atrial Fibrillation (AF). We identified 9,114 magnesium prescribing opportunities (1,914 patients). Approximately one-third of the variation in magnesium supplementation was due to the bedside nurse (see figure below) such that magnesium was supplemented on 48% of occasions where the nurse's habits placed them in the 'liberal' supplementation group versus 28% of occasions with 'conservative' nurses. AF was uncommon overall but decreased by approximately 3% when patient's were cared for by 'liberal' magnesium supplementers.

![Probabilty of magnesium supplementation by bedside nurse](assets/mgbynurse.png)

We will use the pseudonymised reference to the prescriber captured in CCHIC-periop (WP1) to define clinician's prescribing preferences for magnesium and oxygen saturation targets. Because prescribing preference is only one of many factors that affects the treatment decision then there is imperfect compliance. In other words, we are imagining an RCT where the patient's exposure to a pro- or anti- Magnesium 'top-up' clinician is the random coin toss. Other factors may trump the prescriber's preference (i.e. recent arrhythmias) but where the prescriber is otherwise indifferent then their inherent preference will affect the decision. For these marginal cases, we can use an Instrumental Variable (IV) technique to evaluate the causal effect of Magnesium on subsequent arrhythmias.

This method both demonstrates the degree of exising variation in practice, and gives us an initial look at the likely effect size. We would repeat these studies as part of the evaluation pathway for any intervention being considered for PreMEDS+R. This work package builds a robust, reproducible, and repeatable pipeline for generating this evidence. And this evidence then informs the priorities, and design of the prospective evaluations in WP3 and WP5. As CCHIC-Periop expands, the incremental cost of studying additional interventions will decrease. Other suitable targets might include transfusion triggers, oxygen targets, blood pressure targets, and antibiotic duration etc.

## Work package 2C: Statistical simulation procedures
**Objective: To generate the supporting evidence (sample size, nudge design etc.) to transition the observational proposal to a trial protocol**

This proposal is designed to generate a pipeline for rapid evidence generation. This means that each proposal will need to move through a templated series of steps. We will explore and develop methodologies within this work package to this end:

- trial simulation to estimate feasibility. I will leverage existing collaborations to build a Bayesian simulation framework that will take the effect sizes estimated in WP2B via the CPP studies. These will be combined with initial estimates (to be iterated on in WP3) of nudge compliance to generate likely sample sizes. This in turn will be used to select which questions to prioritise and progress
- factorial designs will be preferred where possible to permit evaluation of multiple interventions simultaneousy. The two exemplar questions (magnesium supplementation and oxygen targets) are not expected to have an interactions and would be appropriate for this approach. In all cases, we will nonetheless, need to confirm that the expected variation in practice remains across different factor levels; or set out to deliberately explore anticipated and desired interactions but adjust the sample size accordingly
- trial simulation to explore adaptive thresholds and stopping rules for either efficacy or futility

## Work package 2D+2E: Decision support and randomisation tool implementation
**Objective: To identify the appropriate moment and method to provide decision support (or) randomisation**
We will need to examine where in the clinical workflow the decision point occurs, and what trigger in the electronic record will most appropriately and effectively deliver the nudge. For example, 
- magnesium supplementation is normally delivered in the first few hours of the day shift by the bedside nurse after he or she reviews the magnesium results from night time samples. There are several opportunities to nudge the bedside nurse: at first log on; when the magnesium result is first viewed in the EHR; or at custom times in the day based on known rhythms of work. 
- oxygen saturation targets are often set by the medical team during the daily ward round but may be left to the discretion of the junior clinician, or default to unit targets. Actioning of the target will then depend on the bedside nurse's rhythm of work, when they observe and record SpO2, and when they review the medical guidance. Again, we will need to choose the most appropriate moment to trigger the alert such that it is effective but non-intrusive (and counterproductive)

The ideal any such scenario is for a nudge that guides behaviour as part of the routine workflow such that it reduces cognitive load (as in decision _support_) by providing relevant timely advice. We have an existing collaboration with health design teams, and with the EHRS team here at UCLH. My team are already exploring mechanisms for adapting the existing decision support and embedded randomisation tools for this purpose (through an MRC funded PhD Fellowship). We plan to trial several different strategies in 2021, and evaluate how they affect nudge compliance and impact on work flow. We will in addition explore through interviews and small group discussions with clinicians their views on the delivered nudge. This will provide the foundation for implementation here.

## Work package 2F: Patient and public involvement and transition to opt-out consent
**Objective: Build a patient, public, clinical and academic community to guide the development of this methodology**

My team has already started a series of patient-public involvement panels for this work. Initial meetings have been positive but highlighted the difficulty in explaining the (1) natural variation that occurs with clinical care and (2) why we are not already performing research of this kind. Feedback has suggested that opt-out consent is likely to be acceptable to many, but depends on appropriate communication. We have a small grant from UCLH BRC that we will use to supplement the funds allocated from this proposal to build a dedicated patient and public panel to work with us for the duration of the project. UCLH BRC has expressed interest in this work, and already supports the AboutMe initiative[^c] that also embeds research into the clinical care pathways (focusing initially on stroke and the genomics of hypertension).

Patient and public involvement will be needed to
- define and prioritise questions that might be suitable for the PreMEDS+R design
- design and understand the communication issues necessary to be confident that we have adequate explanations of the risks and benefits of this approach for a wide range of health service users
- design the qualitative interviews that will be conducted in the pilot phase (WP3) that will guide the transition from pre-emptive to opt-out consent
- design the monitoring process that will be used to ensure that PreMEDS+R recruits, the right safeguards are in place to deliver the best evidence from existing literature and from the evolving inputs generated from the trial

We will appoint patient representatives to the project steering committee from the outset. I will deliver a series of focus group meetings that will help use build the communication strategy outlined above, and where necessary create appropriate media (patient information leaflets, posters, videos etc.) that can be used going forwards. I will then report back the qualitative feedback from the pilot trial to this group, and seek their guidance in understanding whether or not I have reached a stage where opt-out consent is a reasonable approach for the question at hand.

## Work package 3A+3B: (3A) A feasibility study with presumed consent transitioning to (3B) a pilot study with opt-out consent
**Objective: A feasibility study to evaluate the PreMEDS+R design**

The two interventions now be worked into a study protocol and submitted for approval by NHS Research Ethics. The purpose of the _feasibility_ study is to prove that the nudge-randomisation tool is technically feasible to implement (that is convert the existing clinical decision support functionality to serve our needs), and that we can deliver an effective PPI framework that will monitor its acceptability (as per WP2). I will work with Epic Systems and the UCL Research Software Engineering team to modify existing decision support tools. The software engineering will be quality controlled to meet necessary standards for health care (ISO 62304 and DCB0129). Continued PPI work (using UCL BRC grant funding) in the form a patient focus group.  Mixed methods approach using surveys, semi-structured interviews and focus group output.

The feasibility study will be a prospective randomised clinical trial using a convenience sample from an appropriate surgical population.  Patients will be recruited from Anaesthetic Pre-assessment Clinic prior to surgery.  At this point decision to undergo surgery will have been taken.  Patients will receive a study information sheet and an explanation of the study from the recruiter.  Following this they will be offered an opportunity to provide (pre-emptive) written consent to the study. The study will then run as per the intended final design: embedded decision support with randomisation (via nudging). However, at this stage, a survey will be delivered to both clinicians and patients along with follow-up qualitative interviews.

The primary outcome will be 
- clinician compliance with the nudge (to adjust the sample size estimates):Number of times in the intervention arm that the clinician agrees to the "nudge", compared with the total number of opportunities to comply i.e. "nudge" efficacy.  Including variance of nudge compliance across treatment groups.
- clinical acceptability of the nudged design

Secondary outcomes will be include:
1. via qualitative semi-structured interview data from patients and families:
    a.	Existing knowledge of variation in practice as a concept.
    b.	The acceptability of an opt-out consent model.
    c.	The acceptability of clinician "nudge" randomisation tool.
2. via qualitative semi-structured interview data from clinicians:
    a.	Existing knowledge of variation in practice as a concept.
    b.	The acceptability of a opt-out consent model.
    c.	The acceptability of clinician "nudge" randomisation tool.

If the estimated rate of nudge 'compliance' is such that the trial could generate evidence in a meaningful time frame _and_ the qualitative feedback from patients and clinicians is supportive then we will proceed to WP3B.

## Work package 3B: A pilot study with opt-out consent
**Objective: Pilot the PreMEDS+R design using opt-out consent; confirm estimates of nudge compliance, recruitment, and effect size; prepare for a major programme grant**

The final piece of work in this proposal will be to see the ideas designed thus far graduate to a full version of the PreMEDS+R design at one or more research sites. Our ambition will be to have applied for funding and support during year 3 for this to run at multiple sites. We think this is reasonable and likely given the evidence that we will have generated by that stage, but do not feel that we can fund such a programme within the scope of this grant alone. For that reason, this final WP is described at UCLH alone. 

The trial itself will continue to run as per WP3A with the single exception of the timing of consent that will move to an opt-out model. This transition will remain a target for active (but tapering) evaluation. In other words, we will purposefully approach a random sample of patients during the early stages of the opt-out model to seek their views on the trial. We will gather evidence to ensure that they understood that they were on a treatment pathway where (1) uncertainty remains for the clinician and that (2) research including randomisation was being employed to reduce this uncertainty and that they (3) were aware of their rights to opt-out.

The trial itself will be designed to prove that we can generate evidence according to the principles outlined. That is:
- embedded within the electronic health record so that
    - there is no additional burden of data collection
    - trial monitoring including adaptive randomisation is delivered through the EHR
- more than one intervention is evaluated simultaneously (e.g. both oxygen saturation targets and magnesium supplementation thresholds)
- compliance with the nudge remains effective but deliberately imperfect indicating that we are identifying the individual moments of equipoise for each bedside clinician but that clinician nonetheless is prepared to override the nudged recommendation when they have relevant and particular knowledge
- compliance with the decision support component remains effective so that unwarranted variation is reduced and treatments are consistent where evidence is available
- that the inefficiency associated with nudged (rather than mandated) randomisation was more than compensated for by the recruitment rates achieved by embedding the randomisation event and allowing each clinician to find their own level of equipoise. 

Success criteria will include
- high levels of awareness of the study among patients on the treatment pathway
- qualitative statements of support from patients who aware of the study
- low levels of withdrawal from participation in the PreMEDS+R pathway 
- consistent and non-trivial rates of compliance with the nudged randomisation 
- recruitment rates that succeed by an order of magnitude those that could be achieved by standard approaches

Stretch goals will include
- successful funding applications to see the study extended to other sites
- new clinical questions entering the beginning of the trial pipeline
- early evidence of treatment effects that allow a treatment arm to be retired either because it has proven inferior or equivalent but more costly

---

# Endnotes

[^a]: This is a more practical statement of theoretical equipoise which may be defined as "a state of uncertainty in the mind of the individual investigator regarding the relative merits of interventions A and B for some population of patients. When investigators are in such a state of uncertainty they do not knowingly disadvantage patients if they allow treatments to be allocated by a process that supports reliable medical inference, such as randomisation."

[^b]: endotypes refer to distinct pathophysiological mechanisms within a disease entity that respond differently to treatments (i.e. create treatment heterogeneity) and therefore justify the idea of 'personalised medicine'

[^c]: https://www.uclhospitals.brc.nihr.ac.uk/about-me


# References
