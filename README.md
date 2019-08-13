# Postfix-Expression-Evaluator
# C++
Evaluate a user inputted RPN expression using stacks.
# Example Input/Output
 Please enter the RPN expression to be evaluated: 9 2 1 + / 4 * :
 Token = 9 Push 9
 Token = 2 Push 2
 Token = 1 Push 1
 Token = + Pop 1 Pop 2 Push 3
 Token = / Pop 3 Pop 9 Push 3
 Token = 4 Push 4
 Token = * Pop 4 Pop 3 Push 12
 Token = Pop 12
 Type 'Y' or 'y' to continue or type any other letter to quit: q
