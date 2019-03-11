Thanks for using EasyAlign!

This software can align python lists of any objects that can be compared with the '==' operator (Notably, strings!)

To use it

Thanks for using EasyAlign!

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
