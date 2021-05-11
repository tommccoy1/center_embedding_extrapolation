# Infinite use of finite means? Evaluating the generalization of center embedding learned from an artificial grammar

This is the repository of materials for the paper "Infinite use of finite means? Evaluating the generalization of center embedding learned from an artificial grammar" by [R. Thomas McCoy](http://rtmccoy.com/), [Jennifer Culbertson](https://jennifer-culbertson.github.io/), [Paul Smolensky](https://www.microsoft.com/en-us/research/people/psmo/), and [Géraldine Legendre](https://cogsci.jhu.edu/directory/geraldine-legendre/).

# Supplement

The complete paper, including the supplementary materials as a set of appendices, can be found [here](http://rtmccoy.com/center_embedding_extrapolation_cogsci_2021_with_appendix.pdf). The supplementary materials include:
- Results of all preregistered analyses
- Analysis of individual participants
- Thorough review of related work

# Experiment code

Our experiment was created using [jspsych](https://www.jspsych.org/), with help from [this template](https://github.com/djnavarro/blankex) by Danielle Navarro. The code for the experiment is in the directpry `experiment/`. You can try out a demo of the experiment [here](http://rtmccoy.com/center_embedding.html).

# Individual results

The results for all individual participants are in the files `all_results.tsv`; the results for the subset of participants who were deemed successful interpolators (see paper for details) are in `successful_interpolator_results.tsv`. These are tab-separated value (.tsv) files; they are viewable on GitHub, but can be viewed less clunkily by opening them in a spreadsheet app such as Google Sheets or Microsoft Excel.

Here is a description of the columns in these results files. Note that an "accurate" response is defined as correctly accepting a grammatical sequence or correctly rejecting an ungrammatical sequence.
- **Participant ID:** A random alphanumeric code identifying the participant.
- **Length 2: Grammatical:** The participant's accuracy on the grammatical test sequences of length 2 (there were 3 such sequences)
- **Length 2: Unrammatical:** The participant's accuracy on the ungrammatical test sequences of length 2 (there were 3 such sequences)
- **Length 4: Grammatical:** The participant's accuracy on the grammatical test sequences of length 4 (there were 5 such sequences)
- **Length 4: Unrammatical:** The participant's accuracy on the ungrammatical test sequences of length 4 (there were 5 such sequences)
- **Length 6: Grammatical:** The participant's accuracy on the grammatical test sequences of length 6 (there were 8 such sequences)
- **Length 6: Unrammatical:** The participant's accuracy on the ungrammatical test sequences of length 6 (there were 8 such sequences)
- **Length 8: Grammatical:** The participant's accuracy on the grammatical test sequences of length 8 (there were 8 such sequences)
- **Length 8: Unrammatical:** The participant's accuracy on the ungrammatical test sequences of length 8 (there were 8 such sequences)
- **Hypothesized rule(s):** The rule(s) which the participant's behavior was consistent with. See below for a list of the rules we considered and the criteria for deciding if their behavior was consistent with that rule.
- **Participant's free response answer:** The participant's answer to a free-response question at the end of the experiment asking what patterns they had noticed. This question was optional, so not all participants have a response.

Here are the rules we considered for the **Hypothesized rule(s)** column. We used 75% as a criterion because this is the lowest score a participant needs (when there are 16 items, which there are in all of the relevant cases) for that score to have a p-value less than 0.05 using a binomial test with the probability of success equal to 0.5 (the chance of successs participants would have if randomly guessing. In the criteria discussed below, the *short subset* refers to the combination of the length-2 and length-4 test sequences, which combined give 16 examples; the *interpolation subset* is the length-6 test items; and the *extrapolation subset* is the length-8 test items. Note that, under the criteria below, it is possible for a single participant's results to be consistent with multiple hypotheses, or might not be consistent with any of the hypotheses.
- **Interp and extrap:** *Rule:* The correct, center-embedded pattern, applied to all sequence lengths (both interpolation and extrapolation). *Criterion:* Participants must score at least 75% on the short subset, at least 75% on the interpolation subset, and at least 75% on the extrapolation subset.
- **Interp only:** *Rule:* The correct, center-embedded pattern for the lengths seen during training, but rejecting all sequences longer than those seen during training. *Criterion:* Participants must score at least 75% on the short subset and at least 75% on the interpolation subset; on the extrapolation subset, they must have labeled at least 75% of the items ungrammatical.
- **Interp extrap good:** *Rule:* The correct, center-embedded pattern for the lengths seen during training, but accepting all sequences longer than those seen during training. *Criterion:* Participants must score at least 75% on the short subset and at least 75% on the interpolation subset; on the extrapolation subset, they must have labeled at least 75% of the items grammatical.
- **All good:** *Rule:* All sequences are grammatical. *Criterion:* Participants must label at least 75% of the short subset grammatical; at least 75% of the interpolation subset grammatical; and at least 75% of the extrapolation subset grammatical.
- **All bad:** *Rule:* All sequences are ungrammatical. *Criterion:* Participants must label at least 75% of the short subset ungrammatical; at least 75% of the interpolation subset ungrammatical; and at least 75% of the extrapolation subset ungrammatical.
- **All good 4 up:** *Rule:* All sequences of length 4 or greater are grammatical; all sequences of length 2 are ungrammattical. *Criterion:* Participants must score at least 75% on the short subset given labels of *grammatical* for the length 4 items and *ungrammatical* for the length 6 items; they must also label at least 75% of the interpolation subset grammatical and at least 75% of the extrapolation subset grammatical.
- **Length less than 8:** *Rule:* All sequences with a length less than 8 are grammatical; all sequences with length 8 are ungrammatical. *Criterion:* Participants must label at least 75% of the short subset grammatical; at least 75% of the interpolation subset grammatical; and at least 75% of the extrapolation subset ungrammatical.
- **No order:** *Rule:* For every word in the sequence, the word it agrees with must also be present; but the order of the words does not matter. Due to the way our examples were generated, this should lead to perfect performance on the short subset, but uniform labeling of the interpolation and extrapolation items as grammatical. *Criterion:* Participants must score at least 75% on the short subset, and must label at least 75% of the interpolation subset and at least 75% of the extrapolation subsect grammatical.


# License

This code is licensed under an [MIT License](https://github.com/tommccoy1/center_embedding_extrapolation/blob/main/LICENSE).



