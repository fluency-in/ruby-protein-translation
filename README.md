# Ruby: Protein Translation

Write a program that will translate RNA sequences into proteins.

Lets write a program that will translate RNA sequences into proteins. [general ref](http://en.wikipedia.org/wiki/Translation_(biology)

RNA can be broken into three nucleotide sequences called codons, and then translated to a polypeptide like so:

RNA: `"AUGUUUUCU"` => translates to

Codons: `"AUG", "UUU", "UCU"`
=> which become a polypeptide with the following sequence =>

Protein: `"Methionine", "Phenylalanine", "Serine"`
 
There are 64 codons which in turn correspond to 20 amino acids; however, all of the codon sequences and resulting amino acids are not important in this exercise.  If it works for one codon, the program should work for all of them.
However, feel free to expand the list in the test suite to include them all.  

There are also four terminating codons (also known as 'STOP' codons); if any of these codons are encountered (by the ribosome), all translation ends and the protein is terminated.

All subsequent codons after are ignored, like this:

RNA: `"AUGUUUUCUUAAAUG"` =>

Codons: `"AUG", "UUU", "UCU", "UAG", "AUG"` => 

Protein: `"Methionine", "Phenylalanine", "Serine"`

Note the stop codon terminates the translation and the final methionine is not translated into the protein sequence.

Below are the codons and resulting Amino Acids needed for the exercise.

Codon                 | Protein
:---                  | :---
AUG                   | Methionine
UUU, UUC              | Phenylalanine
UUA, UUG              | Leucine
UCU, UCC, UCA, UCG    | Serine
UAU, UAC              | Tyrosine
UGU, UGC              | Cysteine
UGG                   | Tryptophan
UAA, UAG, UGA         | STOP

The tests use the Minitest testing framework. To install it run the command:

    gem install minitest

Run the tests with the `ruby` command:

    ruby protein_translation_test.rb

## Resources

If you have never used Minitest, check out [Intro to TDD][tdd] tutorial from Jumpstart Lab.

[tdd]: http://tutorials.jumpstartlab.com/topics/testing/intro-to-tdd.html

## Source

Tyler Long

This exercise is from the [Ruby][ruby] track on [Exercism][exercism]

[exercism]: http://exercism.io
[ruby]: http://exercism.io/languages/ruby



