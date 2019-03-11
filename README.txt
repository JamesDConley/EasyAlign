Thanks for using EasyAlign! :)

You can install with pip!

pip install EasyAlign 

This software can align python lists of any objects that can be compared with the '==' operator (including strings!)

To use it

from EasyAlign import LocalAligner, GlobalAligner
seq1 = [5,  1, 2, 3, 4, 5]
seq2 = [5, 1, 1,  1, 1, 1, 2, 3]
my_local_aligner = LocalAligner(2, -1)
aligned_seq1,  aligned_seq2,  score = my_local_aligner.align(seq1, seq2)
print(aligned_seq1,  aligned_seq2,  score )
my_global_aligner = GlobalAligner(2, -1)
aligned_seq1,  aligned_seq2,  score = my_global_aligner.align(seq1, seq2)
print(aligned_seq1,  aligned_seq2,  score )

If you want to look at more local alignments than just the best scored one you can directly access the score table from the last alignment using my_local_aligner.table - it's a 2d list of integers.  You can then pass the x,y coordinates (seq1 is x, seq2 is y) to my_local_aligner.traceback(x,y) which will return the aligned local sequences that end at that x/y coord.
