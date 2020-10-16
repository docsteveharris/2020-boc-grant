---
title: research summary
export_on_save:
    pandoc: true
output: word_document
date: 2020-01-31
author: Steve Harris
bibliography: references.bib
csl: science-without-titles.csl
---
800 words
Autumn 2020 (COVID version)

# Research Summary

## Problem statement
> The best mechanism to generate generalizable estimates of treatment effect (ie, broader answers) and understand heterogeneity of treatment effect (ie, narrower answers) is to have extremely broad enrolment, ideally representative of the entire breadth of a disease or condition.[@angus2015]
> Derek Angus, JAMA, 2015

Randomised controlled trials (RCTs) are the gold standard for delivering clinical evidence but 'broad enrolment' is near impossible. This is both due to cost, and because their structure imposes a false dichotomy on what are often finely judged clinical decisions. They work well for binary comparisons (e.g. Phase 3 trials), but only offer broad guidance on questions of timing and dose. RCT results are true only on _average_, and if we wish to move toward personalised medicine, to unpick heterogeneity of treatment effects (HTE), and to optimise questions of timing and dose, then we need a new structure that does not forgo the benefits of randomisation.

**REMAP** (**Randomised Embedded Multifactorial Adaptive Platform**) trials provide a partial solution to efficiency and cost by embedding the RCT in the Electronic Health Record (EHR) and efficiently using the sample by adaptively randomising.[@angus2015] However, point of care recruitment and consent remains expensive, and multi-arm trials cannot approach the subtlety needed for personalised medicine.

## Proposal
I propose a modification of REMAP using **nudge theory** that allows randomisation and recruitment using pre-emptive or presumed consent.[@thaler2009] This practical alternative exploits existing variation in practice to deliver randomisation safely, efficiently and at scale. Variation in practice is used as evidence of clinical equipoise: "honest, professional disagreement among expert clinicians" about the best treatment strategy.[@london2018@410] Treatment allocation is nudged not mandated. The nudge is delivered using clincial decision support (CDS) tool within the EHR with one of three effects:

1. Where evidence already exists, the trial alerts the clinician and reduces unwarranted variation.
2. Where evidence is lacking and the clinician _overrules_ the nudge based on their expert knowledge, the trial learns the specific patient characteristics that led to that decision.
3. Where evidence is lacking and the clinician _complies_ with the nudge,  the trial recruits without further cost.

The decision boundaries in (2) and (3) are flexible: different clinicians will find equipoise at different moments. Because equipoise is internally identified, and  not externally and pre-emptively imposed, we recruit broadly and can evaluate non-binary decisions.  The result is an RCT with imperfect compliance: a prospective implementation of a physician prescribing preference study combined with the ideas that underlie Person-centered Treatment (PeT) effects.[@rassen2009c, @Grieve2019] The health care system reduces unwarranted variation, the clinician provides the best current treatment where evidence exists, and the scientist identifies the best future treatment where evidence is lacking.

## A worked example: What is the optimum target oxygen saturation?
The British Thoracic Society (BTS) guidelines recommend an SpO~2~ target of 94-98% in most circumstances[@odriscoll2017], but there is much routine variation.[@post2019] A recent 1000 patient RCT failed to find a benefit from a conservative (low SpO~2~) strategy.[@icu-rox2019] Yet observational studies suggest heterogenous benefit.[@palmer2019a] REMAP-nudge would implement a CDS that nudges for a conservative (SpO~2~ 94%) or liberal (SpO~2~ 98%) target. Targets outside of the BTS range would be nudged in range. Novel subgroups (beyond stroke, myocardial infarct) where expert opinion overruled the nudge would be defined. And if the nudge was followed in just half the cases, REMAP-Nudge would recruit many-fold faster than the largest trial to date (50% of 2,000 ICU admissions/year versus 1000 cases from 21 sites over >2 years).[@icu-rox2019]

## Safe pathways: A trial incubator for REMAP-Nudge 
Classical parallel arm RCTs remain the right tool for evaluation of investigational therapies. Simple Drug A vs Drug B questions are more efficiently and safely answered in small, tightly controlled studies with mandated treatment arms.
REMAP-Nudge is designed for optimisation of existing care. Embedded randomisation creates broad enrolment balancing the imperfect compliance of the nudge. Moving from point of care to presumed consent requires a safe environment to pilot the question. Specifically, we propose building a pathway with the following stages 

1. Patients and health care providers partner to identify areas of variation in practice
2. A retrospective physician prescribing preference study produces an early estimate of treatment effects
3. A simplified prospective pilot trial with pre-emptive consent evaluates the efficacy of the nudge and the acceptability of opt-out consent.

Those questions that graduate from this pathway are then deployed with opt-out consent at scale across different institutions embedded within the electronic health record.

## Implementation and opportunity
I propose building a trial incubator to optimise the management of respiratory failure. This has relevance for severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2), but more enduringly for much of the work that presents to critical care.
I leverage the existing infrastructure of the NIHR Health Informatics programme for Critical Care (CCHIC) that is led out of UCL/UCLH BRC working alongside the DECOVID collaboration (a high quality database COVID-19 co-led by UCLH and University Hospital Birmingham). CCHIC makes routinely collected clinical data at 7 NHS sites available to researchers. DECOVID has already modelled respiratory support in detail.
We update CCHIC to capture pseudonymised identifiers for the clinical decision maker (prescriber) and build the physician prescribing preference studies: observational correlates of the interventional REMAP-nudge approach.


I then build toward a pilot study of REMAP-Nudge. This grant will support development of this programme at a single site (UCLH). However, the architecture will be built to modern interoperability standards so that it is ready for deployment at NHS sites with an EHR. Alternatively, low-fidelity digital implementation such as that effectively deployed by the RECOVERY trial could be implemented.

Final programme deliverables include:

1. A high-quality respiratory failure database built to scale across multiple NHS sites with long-term follow-up via data linkage
2. A pair of exemplar physician-prescribing preference studies 
3. Qualitative and quantitative evidence from a pilot embedded REMAP-Nudge trial 

### Conclusion
By nudging rather than mandating randomisation and operating within existing clinical norms, we create a trial paradigm that scales efficiently. We generate the sample size to study the varying response to different treatments and deliver a personalised treatment strategy that steadily optimises those millions of small decisions. Ultimately, scaling the trial across multiple sites will deliver a world-first: a true learning health care system that optimises processes and pathways of care not normally amenable to standard parallel arm randomised controlled trials (RCTs).

## Clinical questions
We propose focusing on the respiratory management of severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2). In all work, patients and public will be involved (PPI) with the design, and guidance the transition to _presumed_ consent. Whilst I propose two exemplar study questions (SpO~2~ targets and timing of escalation of invasive mechanical ventilation), this proposal is methodological, and contributing PPI may prioritise other questions. We have prepared one 'low' risk and one high 'risk' question. Risk is defined in terms of challenges to delivering the trial.


1. What is the optimum target oxygen saturation?

   The British Thoracic Society (BTS) guidelines recommend an SpO~2~ target of 94-98% in most circumstances[@odriscoll2017], but there is much routine variation.[@post2019] A recent 1000 patient RCT failed to find a benefit from a conservative (low SpO~2~) strategy.[@icu-rox2019] Yet observational studies suggest heterogenous benefit.[@palmer2019a] REMAP-nudge would implement a CDS that nudges for a conservative (SpO~2~ 94%) or liberal (SpO~2~ 98%) target. Targets outside of the BTS range would be nudged in range. Novel subgroups (beyond stroke, myocardial infarct) where expert opinion overruled the nudge would be defined. And if the nudge was followed in just half the cases, REMAP-Nudge would recruit ten-fold faster than the largest trial to date (50% of 10,000 inpatient surgical cases/year versus 1000 cases from 21 sites over >2 years).[@icu-rox2019]

2. What is the optimum threshold for initiation of invasive mechanical ventilation among patients on CPAP?

    The management strategy for respiratory support (RS) in SARS-CoV-2 remains controversial. One approach favours early Invasive Mechanical Ventilation (IMV) citing the ability to minimise Patient Self-Inflicted Lung Injury. The alternative non-invasive support using Continuous Positive Airway Pressure (CPAP) with delayed transition to IMV for those who fail to respond saving both resource and avoiding the inevitable harm accompanying invasive therapy. Whilst more and more centres are now adopting the CPAP first strategy, the question of when to transition to IMV has not been tackled.

The former is low risk because its implementation is simple, and we have good RCT evidence to show that variation is permissible however we expect that there is treatment heterogeneity and permissive hypoxaemia may have benefits for specific subgroups. The latter is high risk because it is a novel area of research which has already polarised the critical care community. However, conventional attempts to define a simple early vs late decision will be problematic as early and late will have different definitions for different clinicians. We argue that the 'nudge-learning' strategy exposes individual clinical equipoise, and allows 'broad enrolment'. The grant proposal focuses on building the methodology for both. If successful, we would envision scaling the pilot studies using exisiting clinical trials networks.


## Implementation
I leverage the existing infrastructure of the NIHR Health Informatics programme for Critical Care (CCHIC) that is led out of UCL/UCLH BRC working alongside the DECOVID collaboration (a high quality database COVID-19 co-led by UCLH and University Hospital Birmingham). CCHIC makes routinely collected clinical data at 7 NHS sites available to researchers. DECOVID has already modelled respiratory support in detail. Within CCHIC, pseudonymised identifiers for the clinical decision maker (prescriber) are captured to build a pair of physician prescribing preference studies (1+2 above): observational correlates of the interventional REMAP-nudge approach.  
I then build toward a pilot study of REMAP-Nudge. This grant will support development of this programme at a single site (UCLH). However, the architecture will be built to modern interoperability standards so that it is ready for deployment at NHS sites with an EHR. Alternatively, low-fidelity digital implementation such as that effectively deployed by the RECOVERY trial could be implemented.

Final programme deliverables include:

1. A high-quality respiratory failure database built to scale across multiple NHS sites with long-term follow-up via data linkage
2. A pair of exemplar physician-prescribing preference studies 
3. Qualitative and quantitative evidence from a pilot embedded REMAP-Nudge trial 

### Conclusion
By nudging rather than mandating randomisation and operating within existing clinical norms, we create a trial paradigm that scales efficiently. We generate the sample size to study the varying response to different treatments and deliver a personalised treatment strategy that steadily optimises those millions of small decisions. Ultimately, scaling the trial across multiple sites will deliver a world-first: a true learning health care system that optimises processes and pathways of care not normally amenable to standard parallel arm randomised controlled trials (RCTs).

---

This is the second time this proposal has been submitted. The first was focused on adapting randomised controlled trials using the advantages of electronic health records and causal inference techniques to optimise learning for peri-operative medicine. That was in January 2020. Just 9 months later, it is inconceivable that we anyone could have realistically predicted the upheavals the world and our healthcare systems have since experienced.
However, the premise of the original proposal has not changed. We still believe that RCTs are unable to deliver the answers we need to the breadth of questions we face. The difference now is that we have a new disease as the focus of our enquiry.

We build our case on the following arguments.

The limits of randomised controlled trials:
1. We acknowledge the RCTs as the gold standard tool for generating clinical evidence.
2. However, they are expensive, and even with a pandemic the rate of evidence generation is frustratingly slow. More importantly, the results of an RCT are only true on _average_. To unpick such heterogeneity of treatment effects (HTE) and deliver personalised recommendations even larger sample sizes are required. 
3. Such sample sizes are unfeasible. Some progress can be made by embedding the trials in EHR systems to minimise the burden of data collection, but this will never be sufficient.
4. Where the target intervention is a novel therapy then RCTs cannot be replaced. However, where the target intervention is a modification of routine care, then existing variation in practice creates an opportunity to implement a 'learning health care system'.

Variation in routine practice is common, and presents a learning opportunity:
1. Variation in practice is evidence of clinical equipoise: "honest, professional disagreement among expert clinicians" about the best treatment strategy.[@london2018@410]
2. Existing retrospective designs known as physician prescribing preference (PPP) studies exploit this variation to make causal statements about treatments. They assume that there was a degree of random chance that led to a patient's encounter with a specific doctor. The hospital you attend depends on whether you are at work or at home when you fall ill. The doctor you meet depends on their shift pattern and holidays etc. Where that doctor exhibits some preference for a treatment decision (e.g. a choice of drug, a recommendation for a procedure, an approach to investigations etc.), then there is randomness in the allocation of treatments that can be exploited. The 'coin toss of a formal RCT' is replaced with the random circumstances that exposed that patient to that doctor's preference.

{{>>
2nd strand to the nudge: RCTs need clear treatment separation; nudge allows us to find each individuals zone of equipoise
Maybe start making the case by asking the reader to consider the concept of equipoise; then talk about equipoise as a continuum; and for a trial there is the idea that you ask clinicians to give up their own individual equipoise and submit to the group uncertainty; this causes ethical issues at the bedside and is a common reason for poor recruitment
<<}}



I propose to merge these two strands of argument. We will modify existing clinical decision support tools to develop and implement a randomised trial that reproduces this routine variation in practice. The deliberate implementation will allow learning at scale. The scale will allow us to explore the treatment heterogeneity that is the achilles heel of the classic RCT. And the insights into treatment heterogeneity will  enable us to deliver targeted and personalised medicine for the benefit of our patients.




## Proposal
**REMAP** (**Randomised Embedded Multifactorial Adaptive Platform**) trials provide a partial solution by embedding the RCT in the Electronic Health Record (EHR) and reducing the cost of data collection.[@angus2015] However, point of care recruitment and consent remains expensive. 
I propose a modification of REMAP using **nudge theory** that allows randomisation and recruitment using pre-emptive or presumed consent.[@thaler2009] This practical alternative exploits existing variation in practice to deliver 
3. For example, 

2. Treatment allocation is nudged not mandated. The nudge is delivered using clincial decision support (CDS) tool within the EHR with one of three effects:

1. Where evidence already exists, the trial alerts the clinician and reduces unwarranted variation.
2. Where evidence is lacking and the clinician _overrules_ the nudge based on their expert knowledge, the trial learns the specific patient characteristics that led to that decision.
3. Where evidence is lacking and the clinician _complies_ with the nudge,  the trial recruits without further cost.




Spring 2020 (BC)



# Research Summary

## Problem statement
Randomised controlled trials (RCTs) are the gold standard for delivering clinical evidence. However, they are expensive and deliver results that are only true on _average_. To unpick such heterogeneity of treatment effects (HTE) and deliver personalised recommendations even larger sample sizes are required. 

> The best mechanism to generate generalizable estimates of treatment effect (ie, broader answers) and understand heterogeneity of treatment effect (ie, narrower answers) is to have extremely broad enrolment, ideally representative of the entire breadth of a disease or condition.[@angus2015]
> Derek Angus, JAMA, 2015

However of the millions of health care decisions most are inacccessible to study by randomisation. Even when the decisions are minor, it is inconceivable that the aggregate effect of poorly optimised routine care is unimportant.

## Proposal
**REMAP** (**Randomised Embedded Multifactorial Adaptive Platform**) trials provide a partial solution by embedding the RCT in the Electronic Health Record (EHR) and reducing the cost of data collection.[@angus2015] However, point of care recruitment and consent remains expensive. 
I propose a modification of REMAP using **nudge theory** that allows randomisation and recruitment using pre-emptive or presumed consent.[@thaler2009] This practical alternative exploits existing variation in practice to deliver randomisation safely, efficiently and at scale. Variation in practice is used as evidence of clinical equipoise: "honest, professional disagreement among expert clinicians" about the best treatment strategy.[@london2018@410] Treatment allocation is nudged not mandated. The nudge is delivered using clincial decision support (CDS) tool within the EHR with one of three effects:

1. Where evidence already exists, the trial alerts the clinician and reduces unwarranted variation.
2. Where evidence is lacking and the clinician _overrules_ the nudge based on their expert knowledge, the trial learns the specific patient characteristics that led to that decision.
3. Where evidence is lacking and the clinician _complies_ with the nudge,  the trial recruits without further cost.

The result is an RCT with imperfect compliance: a more efficient version of a physician prescribing preference study.[@rassen2009c] Treatment effects are recovered using Intrumental Variable (IV) analysis.[@hernan2012a] Regardless of the pathway chosen, the clinician and the trialist both meet their obligation to provide the best current treatment where evidence exists, and identify the best future treatment where evidence is lacking.

## Worked example
Consider the question of target oxygen saturations (SpO~2~) for patients undergoing major surgery. The British Thoracic Society (BTS) guidelines recommend an SpO~2~ target of 94-98% in most circumstances[@odriscoll2017], but there is much routine variation.[@post2019] A recent 1000 patient RCT failed to find a benefit from a conservative (low SpO~2~) strategy.[@icu-rox2019] Yet observational studies suggest heterogenous benefit.[@palmer2019a] REMAP-nudge would implement a CDS that nudges for a conservative (SpO~2~ 94%) or liberal (SpO~2~ 98%) target. Targets outside of the BTS range would be nudged in range. Novel subgroups (beyond stroke, myocardial infarct) where expert opinion overruled the nudge would be defined. And if the nudge was followed in just half the cases, REMAP-Nudge would recruit ten-fold faster than the largest trial to date (50% of 10,000 inpatient surgical cases/year versus 1000 cases from 21 sites over >2 years).[@icu-rox2019]

## Implementation
I leverage the existing infrastructure of the NIHR Health Informatics programme for Critical Care (CCHIC) that is led out of UCL/UCLH BRC. CCHIC makes routinely collected clinical data at 7 NHS sites available to researchers. Pseudonymised identifiers for the clinical decision maker (prescriber) are captured to build a pair of physician prescribing preference studies: observational correlates of the interventional REMAP-nudge approach.  I then build toward a pilot study of REMAP-Nudge. This grant will support development of this programme at a single site (UCLH). However, 
- [ ] TODO replace/addend
the architecture will be built to modern interoperability standards so that it is ready for deployment at NHS sites with an EHR. 
with
for key questions of public health importance it would be possible to implement the same approach as a light-weight 'RECOVERY' style trial ...


Building REMAP-Nudge for peri-operative medicine is advantageous because elective surgery patients pass through a pre-assessment clinic permitting _pre-emptive_ consent.
Patients and public will be involved (PPI) with the design, and guidance the transition to _presumed_ consent. Whilst I propose two exemplar study questions (SpO~2~ and Magnesium targets post-operatively), this proposal is methodological, and contributing PPI may prioritise other questions.

Final programme deliverables include:

1. A high-quality prospective peri-operative medicine database built to scale across multiple NHS sites
1. A high-quality prospective peri-operative medicine database built to scale across multiple NHS sites
2. A pair of exemplar physician-prescribing preference studies 
3. Qualitative and quantitative evidence from a pilot embedded REMAP-Nudge trial with pre-emptive consent to justify moving to an opt-out consent model.

### Conclusion
By nudging rather than mandating randomisation and operating within existing clinical norms, we create a trial paradigm that scales efficiently. We generate the sample size to study the varying response to different treatments and deliver a personalised treatment strategy that steadily optimises those millions of small decisions. Ultimately, scaling the trial across multiple sites will deliver a world-first: a true learning health care system for peri-operative medicine that optimises processes and pathways of care not normally amenable to standard parallel arm randomised controlled trials (RCTs).

