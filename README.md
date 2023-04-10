# infomations-project
This is repository.
It looks like there are some errors in the code:

In the function get_attempts, the variable attempts is not initialized, so it could contain garbage values. You should initialize it to 0 before the do-while loop.

In the function calc_win, the parameters a_range and b_range are declared as float but they are supposed to be int. You should change their types to int.

In the function get_guess_number, the line int number = rand() % (b_range + 1 - a_range) + a_range; should be changed to int number = rand() % (b_range - a_range + 1) + a_range;. This is because the modulo operator % has higher precedence than the addition operator +, so you need to add parentheses to ensure that the subtraction is done before the addition.

In the function exit_game, the parameter choose is declared as a char but it is treated as a string when comparing it to the letters 'Д' and 'д'. You should change the type of choose to char and compare it to the characters 'Д' and 'д' using single quotes.

In the scanf function calls in main, you should change the format specifier %s to %c when reading a single character from the user.

In the printf function call in the get_boo function, the placeholder for the number of remaining attempts should be %d instead of %f.

In the printf function call in the calc_win function, the word "выйгрыш" should be spelled as "выигрыш".

In the printf function call in the update_score function, the word "выйграли" should be spelled as "выиграли".

In the printf function call in the update_score function, the format specifier %f should be changed to %.2f to display the score with two decimal places.

In the printf function call in the get_bet function, the word "введите" should be spelled as "введите".

In the printf function call in the get_bet function, the format specifier %s should be changed to %s\n to add a newline character at the end of the prompt.

In the printf function call in the get_bet function, the word "ставку:" should be spelled as "ставку (от 0 до %.2f$):", where the second placeholder should be replaced with the value of dollars.

In the scanf function call in the get_bet function, you should change the format specifier %f to %lf to read a double value instead of a float.

In the if statement in the get_bet function, you should add a condition to check if the input value is greater than 0 and less than or equal to dollars.

In the else branch of the if statement in the get_bet function, you should add a while loop to consume any extra characters left in the input buffer after the scanf call.

Here's the corrected code:

