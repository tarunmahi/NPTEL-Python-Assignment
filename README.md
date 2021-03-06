# NPTEL-Python-Assignment

<b><i>week 2</i></b>

1.A positive integer m is a sum of squares if it can be written as k + l where k > 0, l > 0 and both k and l are perfect squares.
Write a Python function sumofsquares(m) that takes an integer m returns True if m is a sum of squares and False otherwise.
(If m is not positive, your function should return False.)

2.A string with parentheses is well bracketed if all parentheses are matched: 
every opening bracket has a matching closing bracket and vice versa.
Write a Python function wellbracketed(s) that takes a string s containing parentheses and returns True if s is well bracketed 
and False otherwise.

3.A list rotation consists of taking the last element and moving it to the front.
For instance, if we rotate the list [1,2,3,4,5], we get [5,1,2,3,4]. If we rotate it again, we get [4,5,1,2,3].
Write a Python function rotatelist(l,k) that takes a list l and a positive integer k and returns the list l after k rotations.
If k is not positive, your function should return l unchanged.
Note that your function should not change l itself, and should return the rotated list.


<b><i>week 3</i></b>

1.Define a Python function ascending(l) that returns True if each element in its input list is at least as big as the one before it.

2.Define a Python function alternating(l) that returns True if the values in the input list alternately go up and down
(in a strict manner).

3.A two dimensional matrix can be represented in Python row-wise, as a list of lists:
each inner list represents one row of the matrix. For instance, the matrix would be represented as [[1,2,3],[4,5,6]].
Write a Python function matmult(m1,m2) that takes as input two matrices using this row-wise representation 
and returns the matrix product m1*m2 using the same representation.
You may assume that the input matrices are well-formed and have compatible dimensions.

<b><i>week 4</i></b>

1.Write a Python function histogram(l) that takes as input a list of integers with repetitions and returns a list of pairs as follows:
for each number n that appears in l, there should be exactly one pair (n,r) in the list returned by the function, 
where r is is the number of repetitions of n in l.
the final list should be sorted in ascending order by r, the number of repetitions. 
For numbers that occur with the same number of repetitions, arrange the pairs in ascending order of the value of the number.


2.A college maintains academic information about students in three separate lists.

    Course details: A list of pairs of form (coursecode,coursename), where both entries are strings.
    For instance, [("MA101","Calculus"),("PH101","Mechanics"),("HU101","English")]

    Student details: A list of pairs of form (rollnumber,name), where both entries are strings.
    For instance, [("UGM2018001","Rohit Grewal"),("UGP2018132","Neha Talwar")]
    
	Grades: A list of triples of the form (rollnumber,coursecode,grade), where	all entries are strings.
    For instance, [("UGM2018001", "MA101", "AB"), ("UGP2018132", "PH101", "B"), ("UGM2018001", "PH101", "B")].
    You may assume that each roll number and course code in the grade list appears in the student details and course details, respectively.

Your task is to write a function transcript(coursedetails,studentdetails,grades) that takes these three lists as input and
produces consolidated grades for each student. Each of the input lists may have its entries listed in arbitrary order.
Each entry in the returned list should be a tuple of the form
(rollnumber, name,[(coursecode_1,coursename_1,grade_1),...,(coursecode_k,coursename_k,grade_k)])
where the student has grades for k >= 1 courses reported in the input list grades.
The output list should be organized as follows.
    The tuples shold sorted in ascending order by rollnumber
    Each student's grades should sorted in ascending order by coursecode

<b><i>week 5</i></b>
	
Here are some basic facts about tennis scoring: A tennis match is made up of sets. A set is made up of games.
To win a set, a player has to win 6 games with a difference of 2 games.
At 6-6, there is often a special tie-breaker. In some cases, players go on playing till one of them wins the set with a difference of two games.
Tennis matches can be either 3 sets or 5 sets.The player who wins a majority of sets wins the match (i.e., 2 out 3 sets or 3 out of 5 sets) 
The score of a match lists out the games in each set, with the overall winner's score reported first for each set.
Thus, if the score is 6-3, 5-7, 7-6 it means that the first player won the first set by 6 games to 3, 
lost the second one 5 games to 7 and won the third one 7 games to 6 (and hence won the overall match as well by 2 sets to 1).
You will read input from the keyboard (standard input) containing the results of several tennis matches. 
Each match's score is recorded on a separate line with the following format:
Winner:Loser:Set-1-score,...,Set-k-score, where 2 ≤ k ≤ 5

For example, an input line of the form
Halep:Wozniacki:3-6,6-3,6-3
indicates that Halep beat Wozniacki 3-6, 6-3, 6-3 in a best of 3 set match.
The input is terminated by a blank line.

You have to write a Python program that reads information about all the matches and compile the following statistics for each player:

    Number of best-of-5 set matches won
    Number of best-of-3 set matches won
    Number of sets won
    Number of games won
    Number of sets lost
    Number of games lost 

You should print out to the screen (standard output) a summary in decreasing order of ranking, where the ranking is according to the criteria 1-6 in that order (compare item 1, if equal compare item 2, if equal compare item 3 etc, noting that for items 5 and 6 the comparison is reversed).
You can assume that there are no spaces around the punctuation marks ":", "-" and ",". Each player's name will be spelled consistently and no two players have the same name. 