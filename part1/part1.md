### Part 1 Answers
1. The number 3 will be printed. Since var is used, i has function scope and is visible after the loop (var cannot be a block or loop local).
2. 150 will be printed. Since var is used, discountedPrice has function scope and is visible after the loop (var cannot be a block or loop local).
3. 150 will be printed. Since var is used when declaring finalPrice, it has function scope and is visible inside and outside the for loop in the function (so it will be updated to 150 in the last iteration of the for loop)
4. The list [ 50, 100, 150 ] is going to be returned. This is because in the first iteration of the for loop, the element at index 0 in the list [100, 200, 300] is halved, (1 - discount) = (1 - .5) = .5, to 50. Then multiplied by 100 (5000 now). Then rounded (5000 still), then divided by 100 (50 again). Then the element is pushed to the back of the discounted list []. Thus, each element in  in [100, 200, 300] is going to halved and put into the list named discounted. Finally discounted is returned.
5. error. Since let is used and i is declared and intialized within the cotext of the loop, i is only visible within the loop. Once, the loop exists, i will not be visible. 
6. error. Since let is used and discountedPrice is declared and intialized within the context of the loop, discountedPrice is only visible within the loop. Once, the loop exits, discountedPrice will not be visible. 
7. 150 will be printed. Since let is used to declare finalPrice in the context of the function, it going to be visible in the loop below it and after the loop. As a result, finalPrice is updated in the last iteration of the loop to 150.
8. The function will error out considering the first two log statements, but ignoring those lines, the function will print out the [50, 100, 150] using the same logic as 4. The loop will iterate through each element in prices, apply the discount (halving the intial price in this case) and put it in discounted list. 
9. error. i is only visible inside the for loop since it's declared and initialized inside the for loop using let.
10. error. discountedPrice is only visible inside the loop (since const has a scope just within the block of the loop similar to let).
11. error. finalPrice is defined as a const in the scope of the function so it is visible inside the loop and after it. However, since we reassign a const from 0 to another value, there's going to be an error thown. 
12. [0, 0, 0]. The function will error out and not return anything, but if we got rid of the line inside the loop reassigning finalPrice (declared as const), we will have a list of 3 0s since the loop pushes finalPrice (assigned to 0 before the loop) into discounted 3 times.
13. Notations:
    A. student.name
    B. student['Grad Year']
    C. student.greeting() //why does it print an undefined
    D. student['Favorite Teacher'].name
    E. student.courseLoad[0] // 0 or 1?
14. Arithmetic
    A. Output: '32'  -> '3' is a string and we only have 2 operands (seperated by +) so 2 gets converted to a string '2' and gets concatenated with '3' (JS reads from left to right but doesn't matter in this case). If any of the operands are a string, then the other one gets converted to a string. + is a concatenation operator in this case.
    B. Output: 1  -> subtraction operator only works with numbers so '3' gets converted to the number 3 and subtraction 3 - 2 = 1 is performed
    C. Output: 3  -> null gets converted to 0, and 3 and 0 are added (mathematical operation)
    D. Output: '3null'  -> '3' is a string and we only have 2 operands (seperated by + ) so the null operand gets converted to a string 'null' and gets concatenated (JS reads from left to right but doesn't matter in this case). If any of the operands are a string, then the other one gets converted to a string.
    E. Output: 4  -> addition is being performed so Javascripts converts to numbers. true becomes 1 and adds it to 3. + is not a concatenation operator like before. 
    F. Output 0  -> + is an addition operator (not a concatenation operator like before with strings) so Javascripts converts to numbers. false becomes 0, null becomes 0, and both values get added to 0.
    G. Output: '3undefined'  -> '3' is a string and we only have 2 operands (seperated by +) so undefined gets converted to a string 'undefined' and gets concatenated with '3' (JS reads from left to right but doesn't matter in this case). If any of the operands are a string, then the other one gets converted to a string. + is a concatenation operator in this case. 
    H. Output: NaN  -> we have a - operator so "3" and undefined are going to go through a numeric coversion of 3 and NaN respectively. Then when we try to subtract Nan (not a number) from a number, we are going to get NaN
15. Comparison
    A. Output: true  -> '2' gets converted to the number 2 (since we have a comparison operator with operands that are different types). Then, 2 > 1 is evaluated to true.
    B. Output: false  -> since we have two strings, a dictionary comparison is going to occur. The first char '2' on the LHS is greater than char first char '1' on the RHS so LHS is in fact greater than RHS, so false is outputted.
    C. Output: true  -> we are comparing values of different types and we have a == operator, so a numeric coversion is going to occur. '2' gets coverted to the number 2 and 2 == 2 is performed. Since the two numbers are equal, true is outputted.
    D. Output: false  -> we are comparing values of different types, but we have a === operator that does not perform type conversions. As a result, a string and number are not equal and false is outputted.
    E. Output: false -> we are comparing values of different types and we have a == operator, so a numeric conversion is going to occur. true gets converted to 1 and since 1 does not equal 2, false is outputted.
    F. Output: true  -> values that are intuitively empty (like 0) become false and other values becomes true. Since 0 becomes false intiuitively, it makes sense that Boolean(2) or boolean of any other number for that matter becomes true. Since Boolean(2) becomes true, we have true == true and true is outputted. 
16. == checks inequality and performs type conversion if neccessary (values are different types for example) and === does not perform type conversions and immediately returns false if the values being compared are of different types.
17. Output: How are you?  -> In the if statement, we have 2 == true. Since 2 and true are of different types, a numeric conversion is going to occur where true gets converted to 1. Since 2 does not equal 1, we will move on to the elif containing 2. Since the conditional statement is converted to a boolean value, Boolean(2) is going to be performed. since Boolean(0) is false (it's intuively "empty"), converting any other number to boolean is going to output true. Since we have a true when evaluating the conditional in elif, the line below it will run (console.log('How are you?');).
18. code
19. [6, 8, 10] will be returned by the function modifyArray. First, we pass the array [1,2,3] and the function doSomething into modifyArray (called array and callback within the function modifyArray respectively). Then, the for loop inside modifyArray is used to iterate through each element in the array. Let's take the first iteration for example, 
    1.  the number 1 (the first element in the array passed into modifyArray) and another function is passed into doSomething.
    2.  doSomething then takes num ( equal to 1 in this case), adds 2 to it, and passes the new value 3 into the function passed into it. The function passed into doSomething,named callback in the scope of doSomething, multiplies 3 by 2 and returns 6.
    3.  Then doSomething returns 6 as well and now we are back in modifyArray. 
    4.  The return value of doSomething (6) is pushed into newArr.
Thus, for each element in the array [1,2,3], modifyArray adds 2, multiplies the resulting value by 2, puts it into newArr, and returns newArr.
20. code
21. Output: 1
            4
            1
            2