# About that Henry Ford Hospital study...

A recent study of the effectiveness of Covid-19 treatments by researchers at
the Henry Ford Hospital and Wayne State University
(https://www.ijidonline.com/action/showPdf?pii=S1201-9712%2820%2930534-8) has
received lots of attention and, in my opinion, at least partially unwarranted
criticism.  Representative examples of criticism include a story by STAT news
( [**A flawed Covid-19 study gets the White House's attention--and the FDA
may pay the price**](https://www.statnews.com/2020/07/08/a-flawed-covid-19-study-gets-the-white-houses-attention-and-the-fda-may-pay-the-price/) )
and recent comments by Dr. Anthony Fauci, director of the National Institute of
Allergy and Infectious Diseases in
[**Fauci: Henry Ford Health's hydroxychloroquine study 'flawed'**](https://www.detroitnews.com/story/news/local/michigan/2020/07/31/anthony-fauci-henry-ford-health-hydroxychloroquine-study-flawed/5559367002/).


Criticism of the paper is focussed on the need for carefully designed
randomized clinical trials (RCT) to assess the effect of a treatment.  Of
course RCT is an essential, well-known and well-understood mathematical
technique and should be the primary method of treatment assessment. But
carefully conducted, matched retrospective analyses are important too.

Unfortunately, the first set of results in the paper (Tables 1 and 2 and
Figure 1) present comparison statistics on the raw data.  These comparisons are weak
and inferences from them not easy to make. Figure 1, for instance, illustrates
survival curves comparing unmedicated and HCQ- and AZM-medicated subjects. But
because these data are unmatched, and most of the HCQ-medicated patients also
received steroid treatment, we can't really tell from this picture if the
differences in the curves are due to HCQ or to steroid therapy. This is one of
Dr. Fauci's main criticisms.

I worry that the recent kerfuffle about this paper unfairly diminishes or
dismisses the importance of carefully designed retrospective cohort studies
that use matching methods to help make inferences about data.  The STAT News
piece acknowledges that retrospective analyses can be useful but also pointedly
states that, "Again and again (retrospective studies) have been wrong." Careful
though--one can find cases of treatments approved using evidence from clinical
trials that were later found harmful largely through retrospective analysis.
Matching methods can provide important, large-scale, confirmation of treatment
effectiveness in the real-world, and also catch pathological edge-cases not
thought of in the clinical trials. Matching methods applied to retrospective
data are, in their own right, powerful and immensely useful mathematical tools.


## Matching

  "The goal of matching is to create a data set that looks closer to one that
  would result from a perfectly blocked (and possibly randomized) experiment." -- Gary King


Dr. Fauci's criticism does not apply to the matched comparison shown in Tables
3 and 4 and Figure 2. The matching process in this example controls for
steroid therapy between the treatment (given HCQ) and control (not given HCQ)
arms.  In those results, exactly 84 of 190 total subjects in each arm were
given steroid therapy. That is the point of matching! Matched data control for
differences between subjects, emulating a blocked, and possibly randomized depending
on matching details, design.

Because so many subjects received steroid therapy in this study, it was hard
for the matching process to find lots of subjects *not given* steroids.  This
is part of the reason for the large reduction in study size, from over 2500
total subjects to less than 400. But in this case the reduction in study size
allows us to draw a much better-informed inference about treatment effect
independently of steroid therapy.

To be sure, there are three areas the paper could improve on. In particular:

1. As already mentioned, the comparison statistics in the first set of analyses in Tables 1, 2 and Figure 1 are misleading because they were run on un-matched data. They probably should not be stated at all, or perhaps in an appendix.
2. The matching method is 1:1 propensity-score based, but little else is described. A more thorough description of the precise matching methodology should be stated. And, there are likely more modern methods available like coarsened-exact matching and genetic algorithm matching that might be better to use.
3. Data were matched on dichotomous variables, illustrated in Table 3. That might be fine. Even so, the output of the matched data should show more descriptive statistics on each arm for underlying continuous variables. For example consider subject age, clearly a continuous variable. The matching criterion was Age >= 65 years (yes or no). The output of the matching process should show us at least the mean and median age from each arm. Instead, we only get the count of subjects in each arm meeting the Age >= 65 cutoff. Without more descriptive statistics shown for the matched data, we don't have good sense of how well-balanced the matching output really is.


I strongly believe that, rather than dismiss this paper as "flawed" we should
appreciate the result shown in Figure 2, understanding that it represents only
190 HCQ-treated subjects. And then we should discuss ways to expand this kind
of matched, retrospective analysis to much larger sets of data.
