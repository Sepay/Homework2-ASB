HOMEWORK 2 - ASB

Hello everyone, this script was made as an homework of the subject "Analises de Sequencias Biologicas" also know as ASB.


This script has 3 arguments, so when you execute it, you have to executa them like "./filename.py   Arg1  Arg2  Arg3"
The 3 Arguments are the original filename without the format(if example.fasta then the argument is only example), the ngen for mrbayes and the outgroup you choose, respectively.

This script has 8 functions.

1st - The first one is "nexusBasic", that is going to write all the things necessary in Leave Nexus format. this function uses all 3 arguments and determine the ntax with the lenght of the dictionary and the nchar with the lenght of the first sequence in the dictionary. Returns the nexus file.

2nd -(nomesSeq) This function will read all the lines that have the ">" symbol (Sequences Names) and insert those names in a list. This function also eliminates everything of the line, leaving only the names of the sequences. Returns the list.

3rd -(seqConteudo) It's the opposite of the last function, so searches for the lines in the fasta file that don't have ">", and put them into a list. Also eliminates all the "\n" .Returns this list.

The first 3 have the filename as argument.

4th - (seqCorretas) This one has the list returned in "seqConteudo". From that list, this function concatenates the sequences  until they find a smaller lenght then the one before and insert the concatenates sequence into a new list.This list will have the right sequences to put in the nexus file with the right order. Returns this new list.

5th - (obterDict) - This function will take the lists returned in nomesSeq and seqCorretas as arguments. Creates a dictionary  where it takes them as keys and values,  respectively. Return the dictionary.

6th - (mrBayes) - This function takes the outgroup as an argument and only checks if the outgroup is in the list of the names of the sequences returned in nomesSeq.

7th- (nexustoSTDOUT) -  This function only sends to the stdout.

8th - (eliminarNexus) - this function eliminates the nexus file returned in "nexusBasic" so that the user can create his own file if he wants to. Example: "./filename.py Arg1 Arg2 Arg3 > my_filename.nex

Hope this file helps you.
