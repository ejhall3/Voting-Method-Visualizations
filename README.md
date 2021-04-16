# Voting-Method-Visualizations
MATLAB code used to compute the winner of a given election with visualizations.

NOTE: Citation for rgb function on line 62 of code. Link is provided here for ease of download.
https://www.mathworks.com/matlabcentral/fileexchange/1805-rgb-m
rgb function takes characters and converts them to rgb triplets.

The Election function has three parameters: voters, candidates, and type.
Election(voters,candidates,type)

The voters and candidate’s data type are matrices.

These matrices store the cartesian coordinates of voters and candidates respectively where each row represents a voter or a candidate. For example, a voter matrix with N voters in two-dimensions would be a N-2 matrix, or a candidate matrix with M candidates in five-dimensions would be a M-5 matrix. The number of voters and candidates do not need to be the same, but the number of dimensions used to explain their position on the graph must be the same. 

The type parameter is a string data type and describes the type of election that should be simulated. There are 6 options for this parameter: ‘plurality’, ‘runoff’, ‘approval’, ‘score’, ‘condorcet’, or ‘main’. Each type option corresponds to its respective voting method where the ‘main’ type will perform all five elections at once.

The Election function has two outputs for all election types, namely the final vote tally, and the plots produced. The final vote tally will be printed as a vector for each election type that was chosen, where the ith position in the vector corresponds to the number of votes for the ith candidate in the candidate matrix.
	
 After the user has correctly input the voter and candidate matrices along with an appropriate election type and runs the function, the user will be prompted to list the colors to represent the candidates. Using the standard characters used for MATLAB to represent colors, the user must type in a string to this prompt to determine which colors represent each candidate. The ith color in the string will represent the ith candidate from the candidate matrix. For example, ‘rmcy’ would color the first candidate red, the second magenta, the third cyan, and the fourth yellow. After the user has correctly input the color string, all appropriate outputs will be created. The code I used to convert characters into rgb triplets was borrowed from creator Ben Mitch in an m file titled rgb.m found on MathWorks File Exchange.
