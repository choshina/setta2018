Major:

Review 1
- The method is incomplete: Programs that are fault-free (wrt linearizability) may also have a high-level data race. Thus, I would have expected some description of where false-positives could arise.

有误报吗？

add happen-before citation to sec. 3.1
cite DCAS


Review 3

- In Def. 6, what is SE? When you say “A CDRS satisfies that ...”, do you actually mean “A CDRS SE satisfies that ...”? Otherwise SE comes from nowhere. In the two bullets in the definition, what is the trace following \subset_pre ? Is anything missing here? This is supposed to be one of the most important definitions in the paper. Why is it presented in such a sloppy way?


- Algorithm 1 is unreadable: what is supposed to be the input to the algorithm? The < relation cannot exist itself without mentioning a trace.
Which trace are you referring to? What is e’? I see some natural language explanation of e’ (which also referring to some trace), but you have to formalize it in your algorithm.

Review 4

- I think before presenting the concrete definition of their method, the authors should present the intuitive idea of their method and explain why such intuitive idea would work.

