---
title: Programme plan
export_on_save:
    pandoc: true
output: word_document
date: 2020-10-13
author: Steve Harris
bibliography: references.bib
# csl: plos-medicine.csl
csl: science-without-titles.csl
---
- [ ] TODO target 5000 words
- [ ] TODO @idea can you use a regression discontinuity approach for the threshold investigation for respiratory support

# Title
Embedded Randomised
Nudge-learning and Decision Support
Adaptive
Learning Adaptively from Embedded Random Nudges or Decision Support (LEARNDS)
ERNLDS

REMAP-nudge: leveraging the Critical Care Health Informatics Collaborative to build a learning health care system for peri-operative medicine

- [ ] TODO change the title; talk about eliciting equipoise at scale through a more subtle approach

## Problem statement

1. **Randomised controlled trial are expensive and unable to be deployed to answer the range of questions that most clinicians encounter**

There is near universal agreement that the gold standard for evidence generation in clinical medicine is the randomised controlled trial (RCT). However, RCTs suffer from a series of well rehearsed problems related to cost and efficiency. This limits their scope and generalisability. The cost in time and resource is such that we are afforded the chance to ask only a small number of questions, and often over a period of many years. The consequence is that these questions have to be broad, and resulting answers whilst true on average cannot be personalised or specific.  
Part of the response to these problems has been to develop strategies that minimise the cost of RCTs by __embedding__ them in existing data collection structures such as audit programmes or electronic health record systems (EHRS). Better still the trials are not seen as one-off events focused on evaluation of a single treatment, but are instead seen as a __platform__ for the investigation of a single disease. As a treatment is shown to be less effective than its comparator, that treatment is replaced with a new proposed replacement. Over time, better and better treatments are identified without incurring the delays and set-up costs of a series of separate studies.

- [ ] TODO find some quotes / estimates to support these statements of cost

2. **Learning health care systems implemented without randomisation risk bias**

Learning health care systems "... integrate the practice of medicine and the generation of reliable medical evidence in a way that will promote both continuous learning and evidence based medical practice."[@london2018] Usually a learning health care system stops short of using RCTs as a methodology. Instead, they depend on cycles of observation and intervention: a version of quality improvement's Plan-Do-Study-Act (PDSA) cycle. The interventions are not novel experimental therapies but recommendations from existing practice supported by expert opinion, guidelines and consensus recommendations some but not all of which may be based on RCT evidence.
Typically a panel of performance indicators is devised and tracked. As each intervention is implemented, these indicators are used to evaluate its impact and justify modifications, adjustments or new interventions. Inevitably, these PDSA style cycles cannot meet the standards of objectivity that an RCT can offer. There are prone to the same types of bias observational research must overcome.

3. **Randomised controlled trials are not well adapted for non-binary questions**

A Phase 3 trial comparing a new drug to a placebo is well suited to an RCT. However many questions in medicine are non-binary, and the RCT implementation often loses subtlety.  
This in turn means clinicians lose equipoise. 
Consider, as an example, the ARDSNet study of high versus low tidal volume ventilation, arguably the most famous trial of in critical care.[@ref] This reported that mortality was lower for mechanically ventilated patients if the tidal volume was 6ml/kg rather than 12ml/kg. Critics have often pointed out that the tidal volumes in the 'high' group was excessive.[@laffey2000] But more fundamentally, the trial is structurally unable to define the 'optimum' tidal volume (even on average). For that, we would need a multi-arm trial with patients assigned tidal volume targets ranging from below 6ml/kg up to 12ml/kg (i.e. 4ml/kg, 5ml/kg, 6ml/kg, 7ml/kg ...). Forcing a binary choice has further consequences. The bedside clinicians will often find that they the dichotomy is too stretched for their patient. In other words, they loose equipoise because one or more of the arms is too far from their own judgement (e.g. 6 versus 12 ml/kg). Without equipoise, the clinician cannot with conscience enrol the patient.
A similar critique can be made of strategies that evaluate antibiotic duration, fluid balance, the optimum blood pressure, oxygen targets, or the timing of interventions. All of these are decisions that rest on a 'fine balance' of clinical judgement. 

3. **Variation in practice implies clinical equipoise and treatment heterogeneity** 	

> equipoise[^a]: ... honest, professional disagreement among expert clinicians about the relative clinical merits of interventions A and B for a particular patient population[@london2018] 

Variation in practice is more often associated with poor quality care. One critical summary describes variation as the '60-30-10' problem wherein 60% of care conforms to best practice, 30% is ineffective or wasteful, and 10% is harmful.[@Braithwaite]. But even if we eradicate the harm and reducing the waste, there should still be variation. Where clinicians vary care based on a nuanced interpretation of the best available evidence, this is in line with the founding principles of Evidence Based Medicine (EBM).[Greenhalgh 2014] The evidence is after all only the average truth, and it is the clinician's job to recognise treatment heterogeneity and adapt to the circumstances of the individual patient. 

- > treatment homogeneity versus heterogeneity[@longford1999]:
> - homogeneity: treatment B is superior to treatment A for (almost) everybody in the designated population; 
> - heterogeneity: treatment B is superior to treatment A for an average or typical subject in the designated population. *B may be inferior for a non-trivial proportion of subjects*.

6. **Respiratory support for COVID-19 pneumonia**

There are a lot of unanswered questions, and even with the energy currently being diverted toward COVID-19, existing methodological approaches can only hope to offer broad recommendations.

Many questions in medicine are not binary. Even those questions that are translated into an RCT paradigm of Drug A vs Drug B



# Aim and objective (aka hypothesis)

> When there is genuine equipoise between two commonly used treatments, _not_ doing a point of care trial to find out which has a better risk/benefit profile seems _unethical_. Pragmatic RCTs could enable clinically important questions that can be answered fast based on studies carried out in routine care settings on a full range of participants.

**Learning Health Care Systems in the NHS**. Nuffield Trust Seminar, January 2019[@scobie2020]

## Hypothesis
That there is a portion of clinical care that can be optimised in a methodologically rigorous and ethically sound manner without resorting to standard parallel arm randomised controlled clinical trials.

## Aim
This project aims to develop the framework for a learning health care system for ~~peri-operative medicine~~ the critical care management of acute respiratory failure using established infrastructure at a single site but with a proven ability to scale to multiple sites. 

- [ ] NOTE focus on two aspects of RCTs where the 'nudge' could help
        for the purposes of safely scaling (numbers, presumed or informed consent)
        for the purposes of exposing clinical equipoise where that is normally hard to elicit: cite tracman etc. Approach this by talking about the difficulty of creating a dichotomous choice that seems to be fair
        in both examples we use the prescriber/clinician as the target of the intervention rather than the patient
- [ ] NOTE focus on two subjects: resp failure in the haem-onc / immunocompromise AND COVID

### Deliverables (Work packages)
- [ ] TODO speak with Matthew Sydes: would he be interested in collaborating?
- [ ] TODO speak with Tony in Birmingham about haem-onc
- [ ] TODO: speak with WKW about COVID collaboration (formalise with CCHIC)
- [ ] NOTE: intervention ideas
        - fluid balance
        - oxygen target
        - timing of respiratory escalation

1. Repurposing of the CCHIC database for COVID investigations and work (in collaboration with DECOVID?) ~~A high-quality prospective peri-operative medicine database built to scale across multiple NHS sites~~
2. A pair of exemplar physician-prescribing preference studies
	a. Comparison of conservative versus liberal oxygen targets on post-operative morbidity following high risk surgery admitted to critical care
	b. Thresholds for respiratory escalation ... ~~Comparison of high versus low targets of Magnesium supplementation on post-operative atrial fibrillation following high risk surgery admitted to critical care~~	 
3. A programme of work leading to a pilot embedded randomised controlled trial using a novel _nudge_ design also built to scale across multiple NHS sites (**REMAP-Nudge**)

I provide two worked examples (2a and 2b). However, this proposal is methodological, and other clinical questions would also be suitable, and may be prioritised by the integrated patient and public involvement (PPI) pathway.


# Background

- Matt's Magnesium nudge work
- DECOVID work
- Ed's oxygen work


**Learning health care systems** "... integrate the practice of medicine and the generation of reliable medical evidence in a way that will promote both continuous learning and evidence based medical practice.[@london2018] This programme of work integrates digital health and _nudged_ rather than _mandated_ randomised interventions to create a safe, ethical delivery framework for this oft-cited and yet rarely implemented goal. I specifically focus on optimising the delivery of routine health care where pre-existing variation in practice implies clinical equipoise. The end result would be a system that delivers causally robust personalised treatment effects at scale.

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

## Narrative
- [ ] TODO insert paean to RECOVERY (as good as it can get with RCTs at scale)

**Hundreds of millions of decisions** are made every day by doctors, nurses and allied health professionals. Most decisions are so small and routine that we don't always notice them: do we give paracetamol for a fever? do we target an oxygen saturation of 94% or 98%; do we stop the antibiotics this morning or this afternoon? But it is inconveivable that the aggregate effect of all these decisions is not important.
Randomised controlled trials (RCTs) are our 'go to' method for studying a single decision. But **traditional RCTs are slow, expensive and cumbersome**. Moreover they deliver results that are true on _average_ but not adapted for the individual. Personalised medicine recognises that variations in genotype and phenotype require treatments to be appropriately adapted. With unlimited sample size, such evidence could be generated but the cost would be prohibitive. Machine learning (ML) offers to use 'big data' to derive endotypes[^b] but without randomisation observational research remains vulnerable to bias through unmeasured confounding. This is also true for Artificial Intelligence (AI) techniques such as reinforcement learning.[@palmer2019; @komorowski2018]
Parallel two arm (A vs B) RCTs are now being replaced with intelligent designs such as REMAP (**Randomised Embedded Multifactorial Adaptive Platform**) trials.[@angus2015] This automates data collection by **E**mbedding the trial in electronic health record (EHR). It **A**dapts the randomisation algorithm so that as a signal for benefit or harm emerges patients are preferentially allocated to the best strategy. And finally, **M**ultiple treatments (factors) are evaluated together using the same **P**latform so the cost of setting the trial up is shared. REMAP-CAP is the first attempt at this approach evaluating antibiotics, anti-virals and steroids for Community Acquired Pneumonia (CAP).[@2016a] Nonetheless, this is still a hugely expensive international collaboration recruiting initally 2800 patients across 50 sites over several years.[@2016b]
The final result from REMAP-CAP will true _on average_ but cannot provide the right answer for the each patient who may have an allergy to the 'best' antibiotic, or be more susceptible to the immune suppression induced by the steroids, and so on. This **treatment heterogeneity** is driven by subtle endotypes not exposed by the RCT.[@iwashyna2015a] And herein lies the skill of the clinician. To take that average answer and decide if it applies to the particular situation. But while there is shared expertise, each clinician's personal experience creates variation. 
We normally see such variation as a problem.[@wennberg2011] Electronic Health Record Systems (EHRS) often provide clinical decision support tools to improve compliance with evidence and reduce variation. It is assumed that the busy clinician who is more often unwittingly deviating from a guideline rather than personalising treatment. 
But what if we used decision support to both **reduce variation where strong evidence is available, _and_ to learn from the existing variation where evidence is sparse**.
We call this approach _**nudge learning**_, and propose a methodology called _**REMAP-Nudge**_. This design will ultimately depend on _presumed_ (opt-out) consent to allow the trial to scale, and through scale investigate treatment heterogeneity. However, such a paradigm shift in clinical trial implementation requires a pragmatic and stepped approach. This project proposes a stepped implementation building first (1) a high quality database to confirm treatment variation and capture the rich data needed for an embedded RCT; then (2) a programme of work that carefully evaluates patient and clinician acceptance of a nudge methodology; and (3) implements a pilot REMAP-Nudge trial in high risk surgery to estimate nudge compliance, and likely treatment effect sizes. The design is such that if successful the pilot study will then transform to a multi-site learning health care  programme to optimise care of the high risk surgical patient. 
We argue that this is the perfect domain in which to develop this methodology because **we leverage the anaesthetic pre-assessment clinic** to run the initial work using a _pre-emptive_ rather than presumed consent model.

# Project plan

This 4 year programme will build on two existing programmes. Firstly, the established **Critical Care Health Informatics Collaborative** (CCHIC) programme that holds data on 45000+ adminssions from 10+ NHS ICUs.[@harris2018b] The existing governance and data flows create an opportunity to magnify the influence of the RCOA/BOC grant to scale across multiple sites. Secondly, the **Experimental Medicine Application Platform** (EMAP) at UCLH where we have a proven track record of deploying novel applications in realtime against the hospital wide EHRS. More specifically, my team has spent the last two years building EMAP exactly to enable this sort of work. 
EHR systems alone do not permit innovation and development. They are hampered by vendor lock-in, and by the need to prioritise clinical safety and reliability above all else. EMAP is a data science platform built for the NHS inside the NHS according to the following principles (1) Protection of operational systems by deploying a live mirror of the EHRS (2) Protection of patient privacy by following a 'code-to-data' rather than 'data-to-code' paradigm (3) Health care interoperability to permit cross-site collaboration and (4) Open source to foster a community of practice.

## Work package 1: CCHIC-COVID
**Objective: Build an extension to the Critical Care Health Informatics Collaborative (CCHIC) that focuses on respiratory failure in COVID-19**

The NIHR established the Health Informatics Collaborative in 2014. UCL/UCLH has led the Critical Care theme.[@harris2018b] I have co-led the project (with Singer/Brealey/MacCallum) since 2015. We have ethics (REC 14/LO/103) and CAG approval (14/CAG/1001) plus data sharing agreements for 7 UK sites (including Cambridge/GSTT-Kings/Imperial/Oxford/UCL and now the Royal Marsden and Bristol). Routinely collected clinical data from critical care admissions is transferred to UCL's  ISO/IEC 27001:2013 compliant [data safe haven](https://www.ucl.ac.uk/isd/services/file-storage-sharing/data-safe-haven-dsh) where it is organised, cleaned, linked to Hospital Episode Statistics ([HES](https://digital.nhs.uk/data-and-information/data-tools-and-services/data-services/hospital-episode-statistics)) to define health care utilisation and long term survival, and then made available as resource back to the critical care community.
Since 2015, **we have curated data for >45,000 admissions to critical care with 250 data items and >250 million data points**. This resource has led to a series of publications[@palmer2019a; @meiring2018], and high profile presentations (Hot Topics, Intensive Care Society 2019). We have also launched an educational programme including datathons and training courses for clincal data scientists.[@harris] We have had a favourable review of our ethics (2019 5 year review), and ongoing support at PPI events.

- [ ] TODO extend scope and ethics for COVID
- we will extend the scope of the ethics and the collaboration agreements with participating sites to the same cohort studied under the recent 2^nd^ Sprint National Anaesthesia Project (SNAP-2 EpiCCS: Epidemiology of Critical Care after Surgery).[@moonesinghe2017] That is **patients staying in hospital overnight undergoing a surgical or interventional procedure that requires the prescence of an anaesthetist**.

- [ ] TODO expand data specification to handle both COVID and resp failure in the immunocompromised
- we will expand the data specification to include **key case mix measures for peri-operative medicine** (patient comorbidites, risk factors, surgical procedures, anaesthetic techniques and intra- and post-operative complications) leveraging experience with SNAP-2, PQIP[@wagstaff2019] and NELA[@eugene2018]

- [ ] TODO either drop this or re-orient to highlight PPI thinking
- we will standardise and generate **five high quality outcome measures** from these data (1) mortality (2) length of stay (3) planned and unplanned critical care admission and (4) POMS[@grocott2007] and (5) using the existing CCHIC permissions (HES/ONS) to define health care utilisation and long term survival

- we will add metadata to all drugs, orders, and treatment decisions to capture a pseudonymised identifier for the clinical decision maker to build evidence for variation in practice, and preparatory physician-prescribing preference studies[@rassen2009c]
- the scale and scope of data collection requires hospitals that have integrated Electronic Health Records (EHRs). The interventional arm of the study further requires a working clinical decision support technology. We have already had a favourable response from approaching the Cambridge BRC (see attached letter of support from Dr Ari Ercole). 

- [ ] TODO drop this; you will now need to talk about expanding through EHRS networks that are able to cope with the level of digital maturity necessary for this sort of approach
We would see this CCHIC:Peri-op becoming the _premier international resource for observational studies of high risk surgery and peri-operative medicine_. Just at UCLH trust (including RNTNE, NHNN, WMS) we would expect to recruit >10,000 patients per year. Using the NIHR Health Informatics Collaborative network as a springboard alongside extensive and broad networks developed running SNAP-2/EpiCCS, we would seek funding to expand to further sites during the 4 years.

## Work package 2: REMAP-nudge design
**Objective: (1) Generate evidence of variation in practice using Physician Prescribing Preference studies and (2) Run a feasibilty study to test the REMAP-Nudge design**

We have prepared two worked examples but it should be noted that in the actual project, the interventions to be tested will be developed and selected via a joint clinician/patient/public programme, and not investigator driven. This is especially important given that we will be moving to a presumed consent model, and that we will depend on the clinical workforce to engage with the **nudge** approach. Hence the actual questions to be studied may vary. Further examples might include

- [ ] TODO update to focus on respiratory failure
- Titration of noradrenaline to target mean arterial blood pressure
- Titration of inspired oxygen to target haemoglobin saturation
- Transfusion of packed red cells to target haemoglobin concentrations
- Supplementation of magnesium and potassium based on plasma concentrations
- Fluid balance targeting after elective surgery
- Duration of routine antibiotic therapy following elective surgery

The intervention that is chose will then be worked into a study protocol and submitted for approval by NHS Research Ethics. The purpose of the study is to prove that the nudge-randomisation tool is technically feasible to implement, and that we can deliver an effective PPI framework that will monitor its acceptability.

### Physician Prescribing Preference (PPP) studies

These studies exploit natural variation in practice. A classic example comes from the psychiatry literature where GPs have been show to have consistent preferences for different classes of Selective Serotonin Uptake Inhibitors (SSRIs) and Tricyclic Antidepressants (TCAs).[@davies2013] Patients treatments therefore depended on which GP they attended. Given that GP assignment can be argued to be unrelated to the self-harm/suicide (after controlling for social deprivation etc.) then this permits an evaluation of the relative effectiveness of these drugs. Comparable examples in critial care and peri-operative medicine would include transfusion triggers, oxygen targets, blood pressure targets, and antibiotic duration etc.

- [ ] TODO too technical; rewrite
We will use the pseudonymised reference to the prescriber captured in CCHIC-periop to define physicians prescribing preference as intercept estimates from a multi-level model (e.g. the administration of Magnesium would be the dependent variable with serum Magnesium and previous AF as the independent variables, and the prescriber as a random effect).

Because prescribing preference is only one of many factors that affects the treatment decision then there is imperfect compliance. In other words, we are imagining an RCT where the patient's exposure to a pro- or anti- Magnesium 'top-up' clinician is the random coin toss. Other factors may trump the prescriber's preference (i.e. recent arrhythmias) but where the prescriber is otherwise indifferent then their inherent preference will affect the decision. For these marginal cases, we can use an Instrumental Variable (IV) technique to evaluate the causal effect of Magnesium on subsequent arrhythmias.

This method therefore both demonstrate the degree of exising variation in practice, and gives us an initial look at the likely effect size. We would repeat these studies as part of the evaluation pathway for any intervention being considered for REMAP-nudge.


### Feasibility study

#### Problems with Consent


This phase will undertake a qualitative assessment and analysis directed at the main stakeholders of the project, patients, relatives and clinicians.  This progresses an established programme (i.e. that of CCHIC) of patient and public involvement work in this area.  The focus of the qualitative assessment will be threefold:

1.	Knowledge and attitudes towards variation in practice
2.	Acceptability of the suggested investigative approach, with particular emphasis on the nudge randomisation tool for recruitment (and focusing on clinical acceptance of this approach)
3.	Acceptability of pre-emptive and opt-out consent models

The programme will be wrapped around the test implementation of a the nudge randomisation tool. We will work with Epic Systems and the UCL Research Software Engineering team to modify existing decision suppor tools. The software engineering will be quality controlled so that it is suitable for submission for MHRA approval. Continued PPI work (using UCL BRC grant funding) in the form a patient focus group.  Mixed methods approach using surveys, semi-structured interviews and focus group output.


#### Outputs

The feasibility phase provides grounding for research ethics committee applications but will again serve as a standalone piece of work.  It is anticipated that the output will be suitable for submission to a suitable journal in addition.

**Objective: (1) Generate evidence of variation in practice using Physician Prescribing Preference studies and (2) Run a feasibilty study to test the REMAP-Nudge design**

## Work package 3: REMAP-nudge pilot
**Objective: Pilot the REMAP-nudge design using pre-emptive rather than presumed consent; estimate nudge compliance, recruitment, and effect size; prepare for a major programme grant**


# Endnotes

[^a]: This is a more practical statement of theoretical equipoise which may be defined as "a state of uncertainty in the mind of the individual investigator regarding the relative merits of interventions A and B for some population of patients. When investigators are in such a state of uncertainty they do not knowingly disadvantage patients if they allow treatments to be allocated by a process that supports reliable medical inference, such as randomisation."

[^b]: endotypes refer to distinct pathophysiological mechanisms within a disease entity that respond differently to treatments (i.e. create treatment heterogeneity) and therefore justify the idea of 'personalised medicine'


# References
