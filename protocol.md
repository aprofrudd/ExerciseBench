**ExerciseBench: Development of an expert-moderated benchmark for
evaluating AI exercise advice - protocol for a pilot study**

**Introduction**

Large language model (LLM) chatbots have the potential to provide
high-quality information to support fitness professionals and help
people make evidence-based decisions relating to exercise (D’hoe et al.,
2026). 34% of US adults reported using LLMs for health guidance,
commonly because of speed and their low cost (Kikuchi et al., 2026) and
many use them for specific fitness advice (McVay et al., 2026). LLMs
have demonstrated capability to encode clinical knowledge, and ‘pass’
medical-style examination questions (Singhal et al., 2025). However,
concerns remain about the safety, comprehensiveness, accuracy and
readability of AI-generated exercise recommendations (Zaleski et al.,
2024), whilst the quality of exercise advice depends on contextual
information provided by the user (Düking et al., 2024). To realise the
potential of AI in exercise, it is essential that 1) models behave
safely across diverse, context-dependent situations and 2) there is a
validated field-specific method for evaluating their outputs. Such
methods exist in healthcare, notably HealthBench (Arora et al., 2025)
but no equivalent exists for exercise. A benchmark is a standardised
test for AI models, similar to a fitness test in exercise and allows
different models to be compared and their progress tracked over time.
Therefore, the purpose of this article is to present a pilot protocol
for developing ExerciseBench, an expert-driven benchmark for evaluating
LLM responses to exercise questions.

**Development**

**Principles**

Arora et al. (2025) adopted the following principles in the development
of HealthBench;

1)  Meaningfulness – do scores reflect performance in real-world
    scenarios? In exercise science this relates to ecological and
    content validity.

2)  Trustworthiness – do scores agree with professional judgement? In
    exercise science this relates to inter-rater reliability

3)  Unsaturated – does the benchmark leave headroom for models to
    improve their score and can it differentiate between strong and weak
    responses? In exercise science this would be analogous to selecting
    a fitness test whose ceiling exceeds the performers capacity (e.g.
    Choosing between Yo-Yo level 1 and 2).

**Themes**

As in exercise science, the range of questions posed in healthcare is
vast. To organise these HealthBench grouped them into seven themes, each
representing a distinct challenge from the real-world (e.g. emergency
referral, responding under uncertainty). Themes are therefore categories
of questions and they serve four important purposes; 1) they ensure the
coverage of questions represents common and rare situations; 2) they
enable model strengths and weaknesses in each theme to be identified; 3)
they guide rubric development and 4) determine what the benchmark
assesses. For example a theme could be a topic (such as strength
training) or a behaviour (interpreting a single data point). Topical
themes risk reducing the benchmark to a test of factual knowledge which
would undermine the design principles of meaningfulness and unsaturated,
since knowledge-based tests tend to saturate quickly (Gong et al.,
2025). Behavioural themes are more closely related to professional
judgement. For example, a single data point (e.g. VO2max) cannot be
interpreted without knowledge of how it was acquired, the individual,
day-to-day variation etc.

While HealthBench provides a rationale for each of its themes, the
authors did not report the process they undertook for the generation of
these themes. This limits assessment of their coverage, distinctiveness
and reproducibility. Transparent theme development is important because
it enables methodological quality assessment, a particular concern in
medical AI benchmarking where methods are heterogenous and reporting is
frequently incomplete (Gong et al., 2025).

**Scenarios**

Scenarios represent conversations between a user and an LLM, analogous
to a conversation between a client and an exercise professional. In
HealthBench conversations were developed from three sources. First,
experts wrote seeds describing the types of situations the benchmark
should include. Second a group of experts wrote queries designed to
expose model weakness and third, queries were drawn from HealthSearchQA,
a dataset of frequently searched questions. However, the process by which
seeds were written, how groups selected scenarios or how conversations
were drawn were not described which limits assessment of coverage and
reproducibility. This is important because as a result of this process
an LLM wrote synthetic conversations that were ultimately used to create
the final benchmark.

Themes therefore act as the category, and scenarios are individual items
within the themes. In exercise science this is analogous to aerobic
capacity as a theme, and specific tests to assess aerobic capacity the
scenario. Every scenario belongs to a theme, however the authors of
HealthBench did not describe how a scenario was linked to a theme.

**Rubrics**

HealthBench is a rubric based evaluation tool, whereby a model response
is graded according to a rubric that is specific to a conversation.
Rubric-based approaches have been used to assess LLM responses in
general conversations (Sirdeshmukh et al., 2025), scientific research
(Starace et al., 2025) and clinical settings (Yan et al., 2026). Rubrics
in HealthBench were developed by experts in the field containing the
criteria were required for an ideal answer and what it should avoid.
Criterion were then weighted positively or negatively according to its
importance.

Rubrics are often used in higher education in summative assessments to
grade students work and are usually authored by an individual (e.g.
module leader). HealthBench rubrics were written in a similar way
however, most criteria were not moderated, in academia assessments are
typically internally validated before they are released to students.

**AI grader**

Grading responses at scale is more practical with an AI model (in HealthBench GPT-4.1). For each criterion the grader decided whether a response met it, and it was then graded. To validate the AI grader, physicians marked a sample of responses, and their marks were compared with the AI grader. However, this validation was limited to consensus criteria, a small set of fixed criteria that applied to specific themes which accounted for 14% of all criterion instances, leaving the other 86% unchecked. 

**Pilot Protocol Overview**

The aim of the pilot is to explore the feasibility, time-burden, clarity
of the instructions and estimate of agreement within a protocol that is
unfamiliar within sport and exercise science. Exploring a full protocol
with large recruitment at this stage would increase the risk of
methodological failure.

ExerciseBench uses HealthBench as a basis but is different because it
will use real-questions from experts, moderation at key steps and AI
grader checks.

Progression criteria will be assessed at each phase.

Written in simplified technical English, based on ASD-STE100 for
conciseness

**Phase 0: Ethics**

1.  Get ethics approval before the start

**Phase 1: Collating the themes**

1. Recruit five practitioners
2. Ask the panel what a good answer must do
3. Show panel the draft themes
4. Ask panel to rate each theme for importance (1 to 5)
5. Ask the panel for new themes
6. Ask panel if the wording is clear
7. If 4 out of 5 people say the theme is important keep it
8. Themes are now provisional
9. Ask panel for feedback on the survey

**Progression criteria**: Survey time under 20 min.

**Phase 2: Collecting questions**

1.  Each panel member asked to give 5 realistic questions

**Progression criteria:** More than 20 of 25 are useable

**Phase 3: Sorting questions**

1. Two researchers put each question into one theme. They work independently. 
2. Calculate their agreement (percentage agreement/Cohen’s kappa)
3. Discuss each disagreement and agree a theme
4. Count the questions in each theme to ensure even distribution and fill gaps

**Progression criteria:** Cohen’s kappa \> 0.6 (substantial agreement)

**Phase 4: Writing the rubrics**

1. One theme is randomly selected and the questions in this theme are given to experts
2. Each expert writes criteria for only 2 questions
3. Each criterion describes one behaviour
4. Criterion points range from -10 to +10

**Progression criteria:** Time to write rubrics less than 1 hour

**Phase 5: Moderating the rubrics**

1. Each expert votes on each criterion (approx. 80) except their own: keep, change or remove it.
2. For each criterion, vote on the points: too low, correct or too high.
3. Calculate the agreement (percentage agreement, Krippendorff’s alpha)
4. Keep a criterion if three or more experts vote ‘keep’
5. Record criteria that experts do not agree on
6. Ask feedback on length of task and what was not clear

**Progression criteria:** Krippendorff alpha \> 0.67 (tentative conclusion); \>70% criteria kept; voting time \< 2 hours.

**Phase 6: Test the AI models**

1. Select three AI models (e.g. Gemini 3.5 Flash-Lite, 3.8 Flash and 3.1 Pro)
2. Put each question into each AI (using Jupyter Notebook)
3. Record each answer
4. Give each answer and its rubric to an AI grader (e.g. Claude Opus 5.5)
5. AI grader reads each criterion and answer and records met or not met
6. Calculate score for each answer: points earned divided by maximum points
7. Calculate mean for each model
8. Repeat the test again for stability of the grading model

**Progression:** Grader gives same marks when repeated (95% agreement).

**Phase 7: Check the AI grader**

1. Select a random sample of answers from all models
2. Give the answers to two of three experts
3. Each expert checks each criterion and records ‘met’ or ‘not met’
4. Compare the experts with each other
5. Compare the experts with the AI grader
6. Calculate agreement (percentage and Cohen’s kappa)
7. Record where they do not agree

**Progression:** The AI grader agrees with each expert at least as much as the two experts who agree least.

**After the pilot: Outcomes**

1.  **The method**

    1.  Record number of experts who completed each phase
    2.  Record time of each phase
    3.  Record instructions that were not clear
    4.  For each progression criteria, record the result.

2.  **Expert agreement**

    1.  Report agreement on themes
    2.  Report agreement of sorting questions
    3.  Report agreement on rubric criteria
    4.  Record criteria that experts kept, changed or removed
    5.  Report causes of disagreement

3.  **AI grader**

    1.  Report percentage of marks that stayed the same when AI graded
        again
    2.  Compare grader with each expert
    3.  Compare each expert with other experts
    4.  Record criteria where grader and experts do not agree
    5.  Report causes of disagreement

4.  **AI models**

    1.  Report mean score and range for each model
    2.  Report the number of harmful answers from each model
    3.  Record the criteria that models did not meet
    4.  Find the errors that all models made

5.  **Feedforward for main study**

    1.  Calculate number of questions and experts for main study
    2.  Determine time commitment for experts
    3.  Address issues in rubric-writing
    4.  Review themes
    5.  Find criteria that occur in many situations. Use them as
        standard criteria.

**Example**

**Theme:** Interpretation of single data point.
**Question**: Is 45 ml/kg/min a good VO2max?
Before a criterion is completed, do these checks.
1.  Make sure that the criterion describes one behaviour only
2.  Make sure that a person can mark the criterion ‘met’ or ‘not met’
3.  Make sure the criterion is correct for each person who could ask the
    question. E.g. a young athlete and older adult can ask the same question.
4.  If the criterion has negative points make sure it describes a
    harmful or incorrect answer. Do not give negative answers because you do not like the answer.
5.  Make sure there are no contradictions between criteria.

**Rubric (what must a good answer do):**
1.  Asks how the VO2max was assessed (e.g. lab test, smartwatch
    estimate) +9
2.  Asks for persons age and sex + 8
3.  Explains that 45 depends on age and sex +7
4.  Refers to normative data after extra is sought (e.g. ACSM) + 4
5.  Uses plain language and explains technical terms + 4
6.  States 45 is good or better without qualification – 7
7.  Gives training programme before asking about context – 4
8.  Suggests the value as a diagnosis or health risk for the person -6
**Score = 32**

**References**

Arora, R. K., Wei, J., Hicks, R. S., Bowman, P., Quiñonero-Candela, J.,
Tsimpourlas, F., Sharman, M., Shah, M., Vallone, A., Beutel, A.,
Heidecke, J., & Singhal, K. (2025). *HealthBench: Evaluating Large
Language Models Towards Improved Human Health* (arXiv:2505.08775).
arXiv. https://doi.org/10.48550/arXiv.2505.08775

D’hoe, B., Kirk, D., Boone, J., & Colosio, A. (2026). ChatGPT
Outperforms Personal Trainers in Answering Common Exercise Training
Questions. *Journal of Sports Science & Medicine*, *25*(1), 235–261.
https://doi.org/10.52082/jssm.2026.235

Düking, P., Sperlich, B., Voigt, L., Van Hooren, B., Zanini, M., &
Zinner, C. (2024). ChatGPT Generated Training Plans for Runners are not
Rated Optimal by Coaching Experts, but Increase in Quality with
Additional Input Information. *Journal of Sports Science & Medicine*,
*23*(1), 56–72. https://doi.org/10.52082/jssm.2024.56

Gong, E. J., Bang, C. S., Lee, J. J., & Baik, G. H. (2025).
Knowledge-Practice Performance Gap in Clinical Large Language Models:
Systematic Review of 39 Benchmarks. *Journal of Medical Internet
Research*, *27*(1), e84120. https://doi.org/10.2196/84120

Kikuchi, E., Pasquini, G., & Yam, E. (2026, August 25). From Diagnoses
to Treatments, Why Americans Use AI Chatbots for Health. *Pew Research
Center*.
https://www.pewresearch.org/science/2026/08/25/from-diagnoses-to-treatments-why-americans-use-ai-chatbots-for-health/

McVay, M. A., Willfort, S., Jake-Schoffman, D. E., Dorr, B., Sheer, A.
J., & Henry, K. (2026). *Use of Large Language Models by U.S. Adults to
Support Exercise: A Survey Study* (p. 2026.05.01.26352211). medRxiv.
https://doi.org/10.64898/2026.05.01.26352211

Singhal, K., Tu, T., Gottweis, J., Sayres, R., Wulczyn, E., Amin, M.,
Hou, L., Clark, K., Pfohl, S. R., Cole-Lewis, H., Neal, D., Rashid, Q.
M., Schaekermann, M., Wang, A., Dash, D., Chen, J. H., Shah, N. H.,
Lachgar, S., Mansfield, P. A., … Natarajan, V. (2025). Toward
expert-level medical question answering with large language models.
*Nature Medicine*, *31*(3), 943–950.
https://doi.org/10.1038/s41591-024-03423-7

Sirdeshmukh, V., Deshpande, K., Mols, J., Jin, L., Cardona, E.-Y., Lee,
D., Kritz, J., Primack, W., Yue, S., & Xing, C. (2025). *MultiChallenge:
A Realistic Multi-Turn Conversation Evaluation Benchmark Challenging to
Frontier LLMs* (arXiv:2501.17399). arXiv.
https://doi.org/10.48550/arXiv.2501.17399

Starace, G., Jaffe, O., Sherburn, D., Aung, J., Chan, J. S., Maksin, L.,
Dias, R., Mays, E., Kinsella, B., Thompson, W., Heidecke, J., Glaese,
A., & Patwardhan, T. (2025). *PaperBench: Evaluating AI’s Ability to
Replicate AI Research* (arXiv:2504.01848). arXiv.
https://doi.org/10.48550/arXiv.2504.01848

Yan, Z., Song, D., Fang, Z., Ji, Y., Li, X., Li, Q., & Sun, L. (2026).
*LiveMedBench: A Contamination-Free Medical Benchmark for LLMs with
Automated Rubric Evaluation* (arXiv:2602.10367). arXiv.
https://doi.org/10.48550/arXiv.2602.10367

Zaleski, A. L., Berkowsky, R., Craig, K. J. T., & Pescatello, L. S.
(2024). Comprehensiveness, Accuracy, and Readability of Exercise
Recommendations Provided by an AI-Based Chatbot: Mixed Methods Study.
*JMIR Medical Education*, *10*(1), e51308. https://doi.org/10.2196/51308

