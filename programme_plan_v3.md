
# Title

- [ ] TODO introduce the idea of a 'trial incubator' into the title
REMAP-nudge: leveraging the Critical Care Health Informatics Collaborative to build a learning health care system for COVID-19, critical care and beyond

# Aim and objective (aka hypothesis)

> When there is genuine equipoise between two commonly used treatments, _not_ doing a point of care trial to find out which has a better risk/benefit profile seems _unethical_. Pragmatic RCTs could enable clinically important questions that can be answered fast based on studies carried out in routine care settings on a full range of participants.

**Learning Health Care Systems in the NHS**. Nuffield Trust Seminar, January 2019[@scobie2020]

## REMAP-nudge and COVID-19

This proposal was originally submitted in January 2020 with peri-operative medicine as its target domain.

We argued then that peri-operative medicine was an ideal domain within which to develop this novel methodology, because we could start with a pre-emptive consent model implemented in the pre-assessment clinic, before moving to presumed (opt-out) consent. We built the previous version of this proposal around the evaluation of Magnesium supplementation, and oxygen saturation targets in the peri-operative period. These interventions were selected because they were part of routine care wherein we could already identify variation in practice, where there was no gold standard randomised controlled trial evidence recommending a single approach, and where a there was a reasonable chance that a more personalised treatment approach provide benefit.

We are now resubmitting in October 2020 as we head into the winter with a second surge of SARS-CoV-2 very likely. We continue to believe that the need to develop better methods for improving evidence generation should be the highest priority, and this remains the focus of our application. We recognise that both classical RCTs, and modern interpretations of the RCT (RECOVERY, and REMAP-CAP) are addressing key treatment questions. However, as rehearsed in detail below, these implementations can never hope to provide answers to the full range of scenarios that bedside clinicians must tackle. RECOVERY runs with five treatment arms and recruited 10,000 patients over just a couple of months, and REMAP-CAP with four domains and around 1,500 over a slightly longer time period. These trials are focused evaluations of specific, sometimes novel, sometime repurposed drug treatments. Even together, they address less than ten interventions representing a small fraction of the decisions that constitute the care pathway.

There are no trials evaluating the timing of intubation and ventilation for SARS-CoV-2. We do not know when to prone or stop proning patients. We have no evidence to select a particular PEEP target, nor what level of oxygen saturation is acceptable. The list of questions is almost innumerable. Should we humidify the ventilator circuits? What level of d-dimer would trigger investigation for pulmonary embolism? How much does fluid balance affect the risk of progression to respiratory failure and acute kidney injury? Crucially, even if we did find the resource to study each of these topics in an RCT, the final answer would be incomplete as it is inevitable that what is true on average will not be true for all subgroups. Some patients will tolerate lower oxygen saturations better than others. Some will need a more generous fluid balance.

- [ ] TODO explain that if this route scales across EHRS enabled sites then we can see a 'collaborative' approach to trial development that does scale and does cover the full treatment pathway
This proposal provides a route to answering these questions because we see the task as a process not a project. By taking the principles of REMAP trials but exploiting natural variation in practice to generate the opportunity for randomisation, we are building an evidence generating process. It is a novel step toward a genuine learning health care system. The background and implementation are described in detail below. 

However, here I wish to be clear that whilst we have re-orientated the grant application to COVID-19, I do not wish to create an expectation that we will provide answers that will be relevant to this surge, or even this pandemic. This would be unrealistic for a proposal that runs over four years with a pandemic that evolves week by week. The justification for switching domains is that variation in practice, and therefore the opportunity for learning, is greater when facing a new disease than with established care pathways. Although for different reasons to peri-operative medicine, this too provides a suitable opportunity for developing this approach.

I have kept our original two target questions in this proposal. The oxygen target saturation is clearly and immediately relevant, and suitable targets for supplementation of Magnesium are not defined in general adult critical care. My group has also already developed relevant preparatory work for each, and both questions can be developed under a presumed consent model using the peri-operative care pathway. However, the nature of the implementing a learning health care system involves building an active and genuine collaboration with patients. This means that it is likely that the target questions will be modified as we proceed through the four years. If SARS-CoV remains a major part of our work, then the questions will inevitably address this. If the impact of the pandemic on critical care decreases, then we will still be listening to our PPI partners and adapt similarly adapt the questions as needed.

- [ ] TODO add note about using haem-onc transplant patients as alternative pre-emptive consent pathway with greater probabilty of respiratory complications that would also be relevant to COVID

The grant outputs should therefore be seen as the components of a 'trial incubator' for a learning healthcare system:

1. A high quality prospective respiratory failure database for general adult critical care
2. An exemplar physician prescribing preference (PPP) study that 
    (a) generates early evidence of variation in practice (and)
    (b) causal estimates of treatment effects
3. A pre-pilot pathway that
    (a) evaluates clinician and patient support for presumed consent for the intervention
    (b) generates estimates of nudge compliance
    (c) estimates sample size based on nudge compliance 
4. A pilot trial that demonstrates feasibilty to scale across digitally mature providers

Over 4 years, we would expect that several (2-4) questions would reach Stage 2, that two questions would reach Stage 3, and one question would reach Stage 4. At Stage 4, we would seek additional funding to build the pathway to scaling the study to a partner site (e.g. Cambridge).

## Hypothesis
That there is a portion of clinical care that can be optimised in a methodologically rigorous and ethically sound manner without resorting to standard parallel arm randomised controlled clinical trials.

# Background
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

## Narrative summary

**Hundreds of millions of decisions** are made every day by doctors, nurses and allied health professionals. Most decisions are so small and routine that we don't always notice them: do we give paracetamol for a fever? do we target an oxygen saturation of 94% or 98%; do we stop the antibiotics this morning or this afternoon? But it is inconveivable that the aggregate effect of all these decisions is not important.
Randomised controlled trials (RCTs) are our 'go to' method for studying a single decision. But **traditional RCTs are slow, expensive and cumbersome**. Moreover they deliver results that are true on _average_ but not adapted for the individual. Personalised medicine recognises that variations in genotype and phenotype require treatments to be appropriately adapted. With unlimited sample size, such evidence could be generated but the cost would be prohibitive.
There are two incomplete answers to this problem: machine learning and learning health care systems.  Machine learning (ML) offers to use 'big data' to derive endotypes[^b] but without randomisation observational research remains vulnerable to bias through unmeasured confounding. This is also true for Artificial Intelligence (AI) techniques such as reinforcement learning,[@palmer2019; @komorowski2018]. Learning health care systems "... integrate the practice of medicine and the generation of reliable medical evidence in a way that will promote both continuous learning and evidence based medical practice."[@london2018] However, the LHS also stops short of randomisation and is vulnerable to the same types of bias that all observational research must overcome.
Parallel two arm (A vs B) RCTs are now being replaced with intelligent designs such as REMAP (**Randomised Embedded Multifactorial Adaptive Platform**) trials.[@angus2015] This automates data collection by **E**mbedding the trial in electronic health record (EHR). It **A**dapts the randomisation algorithm so that as a signal for benefit or harm emerges patients are preferentially allocated to the best strategy. And finally, **M**ultiple treatments (factors) are evaluated together using the same **P**latform so the cost of setting the trial up is shared. REMAP-CAP is the first attempt at this approach evaluating antibiotics, anti-virals and steroids for Community Acquired Pneumonia (CAP).[@2016a] Nonetheless, this is still a hugely expensive international collaboration recruiting initally 2800 patients across 50 sites over several years.[@2016b]
- [ ] TODO insert comment on binary evaluations
The final result from REMAP-CAP will true _on average_ but cannot provide the right answer for the each patient who may have an allergy to the 'best' antibiotic, or be more susceptible to the immune suppression induced by the steroids, and so on. This **treatment heterogeneity** is driven by subtle endotypes not exposed by the RCT.[@iwashyna2015a] And herein lies the skill of the clinician. To take that average answer and decide if it applies to the particular situation. But while there is shared expertise, each clinician's personal experience creates variation. 
We normally see such variation as a problem.[@wennberg2011] Electronic Health Record Systems (EHRS) often provide clinical decision support tools to improve compliance with evidence and reduce variation. It is assumed that the busy clinician who is more often unwittingly deviating from a guideline rather than personalising treatment. 
But what if we used decision support to both **reduce variation where strong evidence is available, _and_ to learn from the existing variation where evidence is sparse**.
We call this approach _**nudge learning**_, and propose a methodology called _**REMAP-Nudge**_. This design will ultimately depend on _presumed_ (opt-out) consent to allow the trial to scale, and through scale investigate treatment heterogeneity. However, such a paradigm shift in clinical trial implementation requires a pragmatic and stepped approach. This project proposes a stepped implementation building first (1) a high quality database to confirm treatment variation and capture the rich data needed for an embedded RCT; then (2) builds an observational study capable of generating causal estimates; justifying (3) a programme of work that carefully evaluates patient and clinician acceptance of a nudge methodology; and finally (4) implements a pilot REMAP-Nudge trial for respiratory failure in severe acute respiratory syndrome coronavirus 2 (SARS-CoV-2). The design is such that if successful the pilot study will then transform to a multi-site learning health care  programme to optimise care. The end result of this research programme is a trial incubator that can then see other clinical questions embedded safely into the delivery of care.

# Project plan

## Work package 1: CCHIC-COVID
**Objective: Build an extension to the Critical Care Health Informatics Collaborative (CCHIC) that focuses on respiratory failure in COVID-19**

The NIHR established the Health Informatics Collaborative in 2014. UCL/UCLH has led the Critical Care theme.[@harris2018b] I have co-led the project (with Singer/Brealey/MacCallum) since 2015. We have ethics (REC 14/LO/103) and CAG approval (14/CAG/1001) plus data sharing agreements for 7 UK sites (including Cambridge/GSTT-Kings/Imperial/Oxford/UCL and now the Royal Marsden and Bristol). Routinely collected clinical data from critical care admissions is transferred to UCL's  ISO/IEC 27001:2013 compliant [data safe haven](https://www.ucl.ac.uk/isd/services/file-storage-sharing/data-safe-haven-dsh) where it is organised, cleaned, linked to Hospital Episode Statistics ([HES](https://digital.nhs.uk/data-and-information/data-tools-and-services/data-services/hospital-episode-statistics)) to define health care utilisation and long term survival, and then made available as resource back to the critical care community.
Since 2015, **we have curated data for >45,000 admissions to critical care with 250 data items and >250 million data points**. This resource has led to a series of publications[@palmer2019a; @meiring2018], and high profile presentations (Hot Topics, Intensive Care Society 2019). We have also launched an educational programme including datathons and training courses for clincal data scientists.[@harris] We have had a favourable review of our ethics (2019 5 year review), and ongoing support at PPI events.

Since April 2020, the team at UCLH that built CCHIC have worked on the [DECOVID](https://www.decovid.org) initiative that collates inpatient data from UCLH and University Hospital Birmingham. Substantial time has been invested in capturing a (1) contemporary and accurate description of respiratory failure from the EHRS (e.g. ventilator mode, pressure, volume and flow; airway interventions; rescure therapies etc.) We are simultaneously updating the research governance for CCHIC to allow us to capture (2) all patients with or at risk of respiratory failure during the COVID-19 pandemic. We will also add metadata to all drugs, orders, and treatment decisions to capture a (3) pseudonymised identifier for the clinical decision maker to build evidence for variation in practice, and preparatory physician-prescribing preference studies[@rassen2009c]

We will draw these three strands together to build an extension to CCHIC that focuses on respiratory failure, and specifically SARS-CoV-2.

## Work package 2: Physician prescribing preference studies

These studies exploit natural variation in practice. A classic example comes from the psychiatry literature where GPs have been show to have consistent preferences for different classes of Selective Serotonin Uptake Inhibitors (SSRIs) and Tricyclic Antidepressants (TCAs).[@davies2013] Patients treatments therefore depended on which GP they attended. Given that GP assignment can be argued to be unrelated to the self-harm/suicide (after controlling for social deprivation etc.) then this permits an evaluation of the relative effectiveness of these drugs. Comparable examples in critial care and peri-operative medicine would include transfusion triggers, oxygen targets, blood pressure targets, and antibiotic duration etc.

- [ ] TODO too technical; rewrite
We will use the pseudonymised reference to the prescriber captured in CCHIC to define physicians prescribing preference as intercept estimates from a multi-level model (e.g. the administration of Magnesium would be the dependent variable with serum Magnesium and previous AF as the independent variables, and the prescriber as a random effect).

Because prescribing preference is only one of many factors that affects the treatment decision then there is imperfect compliance. In other words, we are imagining an RCT where the patient's exposure to a pro- or anti- Magnesium 'top-up' clinician is the random coin toss. Other factors may trump the prescriber's preference (i.e. recent arrhythmias) but where the prescriber is otherwise indifferent then their inherent preference will affect the decision. For these marginal cases, we can use an Instrumental Variable (IV) technique to evaluate the causal effect of Magnesium on subsequent arrhythmias.

This method both demonstrates the degree of exising variation in practice, and gives us an initial look at the likely effect size. We would repeat these studies as part of the evaluation pathway for any intervention being considered for REMAP-nudge.

- [ ] TODO review Matt's work and see if you can include this as a 'worked example' (with figures etc.)
