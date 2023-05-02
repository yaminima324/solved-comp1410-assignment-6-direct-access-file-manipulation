Download Link: https://assignmentchef.com/product/solved-comp1410-assignment-6-direct-access-file-manipulation
<br>
In this assignment you are asked to develop a C program that will input character data sequentially from a text file, convert the input to machine compatible formats for storage within a structure, store the structures as binary records in a direct access file and then perform a sort of the direct access file records before producing a formatted output to stdout.  In addition, you will determine the total number of bytes containing in the input file and in the direct access file and output those values for comparison.  You should note that character (i.e. text) files typically require much more storage than binary files due to the fact that binary files store data in the actual machine format, or representation, of various data types.

<strong>Steps: </strong>

<ol>

 <li>In order to test your program, prepare a text file for input – you should call it <strong>dat</strong>. The input file must consist of at least 10 lines of data.  Each line begins with a 6 digit ID that must be unique, as well as 10 arbitrary float values from 0.0 to 100.0.  Each value must be separated from the following value by at least one space character, except the last one which is followed by the end-of-line.  This file represents a set of student grades for each student in 10 courses (assume the same courses for all students)</li>

</ol>

The following steps all pertain to the C program you must write

<ol start="2">

 <li>Declare and initialize all variables, data structures and file structures you will need for this program. You will need a structure with members for storing the unique ID (int), the 10 course marks (array of float), and the GPA (float).You will also need variables to count the number of bytes in the input text file and output binary file.</li>

 <li>For each input text file record, input the entire string – use either gets() or fscanf(). Once the string has been inputted you can determine its length using strlen().  You will need to extract each of the data fields to populate (i.e. transfer data to) the structure members for the ID and marks – you might want to use sscanf() for this task.  At this time you can calculate the GPA and store it in the structure.</li>

 <li>Once you have populated a structure, you should then output the structure to a binary file called <strong>dat</strong>. Determine the size of the structure, in bytes, using the <strong>sizeof</strong> pre-processor operator, and add this to the total count of bytes used in the binary file.  If there is no more data in the input file you should continue to the next step, but if more data exists then you must repeat steps 3 and 4.  You must not use an array to input all data; instead, you must process each input record separately before proceeding to the next.</li>

</ol>




<ol start="5">

 <li>With all of the data outputted to the binary file, you must now perform a sorting operation on the records, so that after the sort is finished, all the records in the binary file are sorted in ascending order by ID. Note that to perform this sort you will likely need at least 2 different structures to read in binary records to do the comparison needed, and then restore the records in required order.  You may use any sort algorithm but a selection sort might be simplest.  For this part, you <u>must not</u> use any other files – your sort must be<u> in place</u> (i.e. within the binary file itself).</li>

</ol>




<ol start="6">

 <li>The final output from your program must consist of the sorted records of student marks, including their GPA, on one output line for each record. Following this, you must output the total number of bytes inputted to the program from file <strong>dat</strong>, as well as the total number of bytes required to store all data in structures stored in the binary file <strong>assign6out.dat</strong>.  Direct your final output to the file <strong>assign6results.dat</strong>.</li>

</ol>


