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
I leverage the existing infrastructure of the NIHR Health Informatics programme for Critical Care (HIC-CC) that is led out of UCL/UCLH BRC, and the RCoA/UCL Centre for Perioperative Medicine (CPOM) led SNAP-2 study. HIC-CC makes routinely collected clinical data at 7 NHS sites available to researchers. SNAP-2 brings a data set for inpatient surgery successfully implemented at 245 NHS sites. Pseudonymised identifiers for the clinical decision maker (prescriber) are captured to build a pair of physician prescribing preference studies: observational correlates of the interventional REMAP-nudge approach.
I then build toward a pilot study of REMAP-Nudge. This grant will support development of this programme at a single site (UCLH). However, the architecture will be built to modern interoperability standards so that it is ready for deployment at NHS sites with an EHR. 
Building REMAP-Nudge for peri-operative medicine is advantageous because elective surgery patients pass through a pre-assessment clinic permitting _pre-emptive_ consent. Patients and public will be involved (PPI) with the design, and guidance the transition to _presumed_ consent. Whilst I propose two exemplar study questions (SpO~2~ and Magnesium targets post-operatively), this proposal is methodological, and contributing PPI may prioritise other questions.

Final programme deliverables include:

1. A high-quality prospective peri-operative medicine database built to scale across multiple NHS sites
2. A pair of exemplar physician-prescribing preference studies 
3. Qualitative and quantitative evidence from a pilot embedded REMAP-Nudge trial with pre-emptive consent to justify moving to an opt-out consent model.

### Conclusion
By nudging rather than mandating randomisation and operating within existing clinical norms, we create a trial paradigm that scales efficiently. We generate the sample size to study the varying response to different treatments and deliver a personalised treatment strategy that steadily optimises those millions of small decisions. Ultimately, scaling the trial across multiple sites will deliver a world-first: a true learning health care system for peri-operative medicine that optimises processes and pathways of care not normally amenable to standard parallel arm randomised controlled trials (RCTs).
