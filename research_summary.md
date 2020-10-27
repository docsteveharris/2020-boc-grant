---
title: research summary
export_on_save:
    pandoc: true
output: word_document
date: 2020-10-26
author: Steve Harris
bibliography: references.bib
csl: science-without-titles.csl
---

# Research Summary: PreMEDS(R)

## Problem statement

> The best mechanism to generate generalizable estimates of treatment effect (ie, broader answers) and understand heterogeneity of treatment effect (ie, narrower answers) is to have extremely broad enrolment, ideally representative of the entire breadth of a disease or condition.[@angus2015]
> Derek Angus, JAMA, 2015

Randomised controlled trials (RCTs) are the gold standard for clinical evidence but 'broad enrolment' is near impossible. This is both due to cost, and because RCTs typically imposes a false dichotomy on finely judged clinical decisions. The resuls are true but only on _average_. If we wish to personalise medicine, to optimise the many small decisions we make, to unpick heterogeneity of treatment effects (HTE), then we need a new structure that does not forgo the benefits of randomisation.

**REMAP** (**Randomised Embedded Multifactorial Adaptive Platform**) trials provide a partial solution by embedding the RCT in the Electronic Health Record (EHR) and efficiently using the sample by adaptively randomising.[@angus2015] However, point of care recruitment and consent remains expensive, and even multi-arm trials cannot approach the subtlety needed for personalised medicine.

## Proposal
I propose a modification of REMAP using **nudge theory** that allows randomisation and recruitment using pre-emptive or presumed consent.[@thaler2009] This practical alternative exploits existing variation in practice to deliver randomisation safely, and efficiently. Variation in practice provides evidence of clinical equipoise: "honest, professional disagreement among expert clinicians".[@london2018@410] Treatment allocation is nudged not mandated. The nudge is delivered using clincial decision support (CDS) tool within the EHR with one of three effects:

1. Where evidence already exists, the trial alerts the clinician and reduces unwarranted variation.
2. Where evidence is lacking and the clinician _overrules_ the nudge based on their expert knowledge, the trial learns the specific patient characteristics that led to that decision.
3. Where evidence is lacking and the clinician _complies_ with the nudge, the trial recruits without further cost.

The decision boundaries in (2) and (3) are flexible: different clinicians will find equipoise at different moments. Because equipoise is internally identified, and  not externally and pre-emptively imposed, we recruit broadly and can evaluate non-binary decisions. The result is an RCT with imperfect compliance: a prospective implementation of a physician prescribing preference study combined with the ideas that underlie Person-centered Treatment (PeT) effects.[@rassen2009c, @Grieve2019] The bedside clinician delivers the best current treatment where there is evidence; and the scientist identifies the best future treatment where there is none.

## A worked example: What is the optimum target oxygen saturation?
The British Thoracic Society (BTS) guidelines recommend an SpO~2~ target of 94-98% in most circumstances[@odriscoll2017], but there is much routine variation.[@post2019] A recent 1000 patient RCT failed to find a benefit from a conservative (low SpO~2~) strategy.[@icu-rox2019] Yet observational studies suggest treatment effects within subgroups.[@palmer2019a] PreMEDS-R would implement a CDS that nudges for a conservative (SpO~2~ 94%) or liberal (SpO~2~ 98%) target. Targets outside of the BTS range would be nudged in range. Novel subgroups (beyond stroke, myocardial infarct) where expert opinion overruled the nudge would be defined. And if the nudge was followed in just half the cases, PreMEDS-R would recruit many-fold faster than the largest trial to date (50% of 2,000 ICU admissions/year versus 1000 cases from 21 sites over >2 years).[@icu-rox2019]

## Safe pathways: A trial incubator
PreMEDS-R is designed for optimisation of existing care. Moving from point of care to presumed consent requires a lightweight but safe pathway:

1. Patients and health care providers partner to identify questions suitable for this approach
2. Retrospective physician prescribing preference studies produce early estimates of treatment effects
3. A pilot trial with _pre-emptive_ consent evaluates (a) the efficacy of the nudge and (b) the acceptability of opt-out consent.

Questions that graduate from this pathway are then deployed with opt-out consent at scale. This grant will support development of this programme at a single site (UCLH) but using modern interoperability standards ready for deployment at other digitally mature NHS sites.

## Implementation
I leverage both the existing infrastructure of the NIHR Critical Care Health Informatics Collaborative (CCHIC) led out of UCL/UCLH BRC, and the RCoA/UCL Centre for Perioperative Medicine (CPOM) led SNAP-2 study. CCHIC makes routinely collected clinical data at multiple NHS sites available to researchers. SNAP-2 brings a data set for inpatient surgery successfully implemented at 245 NHS sites. Pseudonymised identifiers for the clinical decision maker (prescriber) will be captured to study variation in practice. We leverage the pre-assessment clinic to for pre-emptive consent. Whilst I propose two exemplar study questions (SpO~2~ and Magnesium targets post-operatively), this proposal is methodological, and contributing PPI or the COVID-19 response may prioritise other questions.

### Conclusion
By nudging rather than mandating randomisation and operating within existing clinical norms, we create a trial paradigm that scales efficiently. We generate the sample size to study the varying response to different treatments and deliver a personalised treatment strategy that steadily optimises those millions of small decisions.


