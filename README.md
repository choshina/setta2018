Major:

Review 1
- The method is incomplete: Programs that are fault-free (wrt linearizability) may also have a high-level data race. Thus, I would have expected some description of where false-positives could arise.

- Timing information for the tools should have been presented. Since this is an incomplete method, I would have expected the search to be scale to more than two threads. Is this possible?


- Please do not refer to \sqsubset_S as a "happens-before" relation. This confuses matters (e.g., in relation to weak memory). It would be better to call this the real-time order, as is common in the literature.


- I think the authors could do more to analyse algorithms that haven't been reported in the literature already. For the algorithms analysed, it would be good to see references to the original reports that describe the bugs found. E.g., for SNARK, please reference:
S. Doherty et al: DCAS is not a silver bullet for nonblocking algorithm design. SPAA 2004: 216-224

- Sect 5.1, l2. "Surely the linearizability of .... Besides, we define a state, ..." I found these two sentences confusing. Please rewrite.


Review 2

- My only issue is that I wanted to know a little bit more about the subjects of empirical evaluation, mostly to get the sense of scalability. Table 1 does not contain much details of the subject themselves, nor the number of threads used for each program. As such, it is difficult to see how the scalability trend will look like, when either the size of the program or the number of threads increases. If authors can include these details for the camera ready version, I believe the paper will be much stronger.

Review 3

-  In Def. 5, are the 3rd and 4th bullets saying the same thing? What do you mean by “no temporal relation”? Is the next bullet (the 4th) trying to define “no temporal relation”?
- Page 9, 2nd paragraph below Def. 5, the \subset should be \subset_pre instead?
- In Def. 6, what is SE? When you say “A CDRS satisfies that ...”, do you actually mean “A CDRS SE satisfies that ...”? Otherwise SE comes from nowhere. In the two bullets in the definition, what is the trace following \subset_pre ? Is anything missing here? This is supposed to be one of the most important definitions in the paper. Why is it presented in such a sloppy way?
- Example 4: what do you mean by “#1 wins”? According to you definition before, you only say “e1 wins e2 **with respect to ... Sf **”. Here which sf are you referring to?
- Algorithm 1 is unreadable: what is supposed to be the input to the algorithm? The < relation cannot exist itself without mentioning a trace.
Which trace are you referring to? What is e’? I see some natural language explanation of e’ (which also referring to some trace), but you have to formalize it in your algorithm.
- Fonts in Figs. 6-8 are too small, which make the figures unreadable.

Review 4

- I think it is better to give a symbol table to help readers follow the definitions.
- I think before presenting the concrete definition of their method, the authors should present the intuitive idea of their method and explain why such intuitive idea would work.
- They should also present some basic information of the programs, such as the size, where is each test case from. Since some test cases are from prior work, it is better to compare this method to some previous studies. I note that there also exist other situations where the authors’ method cannot point out exactly. What is the reason for that? I think the authors should explain more about the failure of their method and discuss what are the advantages and disadvantages in using this method in real scenarios.
