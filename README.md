Major:

- The method is incomplete: Programs that are fault-free (wrt linearizability) may also have a high-level data race. Thus, I would have expected some description of where false-positives could arise.

Timing information for the tools should have been presented. Since this is an incomplete method, I would have expected the search to be scale to more than two threads. Is this possible?Please do not refer to \sqsubset_S as a "happens-before" relation. This confuses matters (e.g., in relation to weak memory). It would be better to call this the real-time order, as is common in the literature.


I think the authors could do more to analyse algorithms that haven't been reported in the literature already. For the algorithms analysed, it would be good to see references to the original reports that describe the bugs found. E.g., for SNARK, please reference:S. Doherty et al: DCAS is not a silver bullet for nonblocking algorithm design. SPAA 2004: 216-224Sect 5.1, l2. "Surely the linearizability of .... Besides, we define a state, ..." I found these two sentences confusing. Please rewrite.