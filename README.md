Download Link: https://assignmentchef.com/product/solved-csce1030-project
<br>
In this project, you have to write a C++ program to keep track of banking transactions in multiple disk files.

Your objective is to get transactions from a user and process the transactions for debiting or crediting the account. Each user holds two accounts – a business account and a personal account.




You are provided the following files. Download them and view their contents.

<strong>account_data</strong>: This file contains the account name and the account number. The name and the number are separated by a comma.

<strong>145268p</strong>: This file contains the personal transactions made by the account number 145268. If you look at the account_data.dat file, you will see this account belongs to John Smith. <strong>145268b</strong>: This file contains the business transactions made by the same account.




You may choose to create your own transaction files with arbitrary data to test your program for different accounts.

This is an extension of Projects 1 and 2 so you may reuse any work you have done for Projects 1 and

2.




<h1>PROGRAM REQUIREMENTS</h1>

<ol>

 <li>As with all projects in this course, your program’s output will display your name, your EUID, your e-mail address, the department name, and course number. This means that your program will print this information to the terminal (see the sample output).</li>

</ol>




<ol start="2">

 <li>Declare and initialize the following global parameters.

  <ul>

   <li>A global integer constant to store the length of account number and initialize it to 6.</li>

   <li>An enumeration constant with values <strong>Business</strong> and <strong>Personal</strong> and assign integer values 0 and 1 to the data items, respectively. They represent the type of bank account.</li>

   <li>Another enumeration constant with values <strong>Add</strong>, <strong>Remove</strong>, <strong>Process</strong>, <strong>Display,</strong> and <strong>Quit</strong>, and assign integer values 1, 2, 3, 4 and 5 to the data items, respectively. They represent menu choice presented to the user.</li>

   <li>A structure named <strong>Account</strong> with the following members. o Name of the account o Number of the account</li>

  </ul></li>

</ol>

o Type of the Account (i.e. Business or Personal)

➢ You must use a suitable enum type variable for this member.

<ol start="3">

 <li>In your <strong>main</strong> function:

  <ul>

   <li>Display a menu for the user (SEE SAMPLE OUTPUT) that provides the user the following choices.</li>

  </ul></li>

</ol>

o Add a new account o Remove an existing account o Process new transaction on an account o Display the stored transactions on an account. o Quit the program

Using a suitable message, ask the user to make the menu choice using an integer variable.

<ul>

 <li>Based on the value entered by the user for menu choice, design a switch-case block to implement the following requirements.

  <ul>

   <li>You must use the enumeration constants to set up your cases. o You must use a variable of your enumeration constant type for switching control.</li>

   <li>If the user chooses to add an account

    <ul>

     <li>Call the function <strong>addAccount</strong> o If the user chooses to remove an account</li>

     <li>Using a suitable message, ask the user the account number of the account to remove.</li>

     <li>Call the function <strong>removeAccount</strong> and pass the account number entered by the user.</li>

    </ul></li>

  </ul></li>

</ul>

o If the user chooses to process transactions for an account

<ul>

 <li>Using a suitable message, ask the user the account number of the account to process transactions for.</li>

 <li>Call the function <strong>processAccount</strong> and pass the account number entered by the user.</li>

</ul>

o If the user chooses to display transactions for an account

<ul>

 <li>Using a suitable message, ask the user the account number of the account to display transactions for.</li>

 <li>Call the function <strong>displayAccount</strong> and pass the account number entered by the user.</li>

</ul>

o  If the user choose to quit the program.

➢ Exit the program with a suitable message.

o If the user chooses anything else, execute the default case to notify the user an incorrect choice.

<ul>

 <li>Using a suitable loop, ask the use for the choice again.</li>

 <li>Your program must keep on looping until the user enters the correct choice</li>

</ul>




<ol start="4">

 <li>Write a function named <strong>getName</strong> which gets the name on the bank account. Inside the function:

  <ul>

   <li>Using a suitable message, prompt the user for the name on the account. The name can have multiple words.</li>

   <li>Only alphabets (A-Z or a-z) and whitespaces are permitted in the account name.

    <ul>

     <li>If the user enters any other characters in the name, you need to generate an error message and ask for the name again.</li>

     <li>Your program must keep on asking the user to enter the name until the user enters it correctly.</li>

    </ul></li>

   <li>The user may type the name in either uppercase or lowercase, but you need to convert every initial to uppercase.</li>

   <li>This function will be called by the <strong>addAccount</strong></li>

  </ul></li>

 <li>Write a function named <strong>getAccountNumber</strong> which get the account number. Inside the function:

  <ul>

   <li>Using a suitable message, prompt the user for the number of the account.</li>

   <li>The account number must be a 6-digit number.</li>

   <li>If the user enters an account number with more than 6 digits generate an error message and ask the user to enter the number again.</li>

  </ul></li>

</ol>

Only numbers 0-9 are permitted in the account number. If the user enters an account number with non-numeric characters, generate an error message, and ask the user to enter the number again.

<ul>

 <li>Your program must keep on asking the user to enter the number until the user enters it correctly.</li>

 <li>This function will be called by the <strong>addAccount</strong></li>

</ul>




<ol start="6">

 <li>Write a function named <strong>getNumberofTrasanctions</strong>. It accepts a string that stores the filename of a disk file and return an integer representing the number of transactions in the disk file.

  <ul>

   <li>Inside the function, open the file for reading using the filename passed to the function.</li>

   <li>Count the number of transactions in the file.</li>

   <li>For example, the file <strong>145268b</strong> has <strong>7</strong> Hence the name of the file <strong>145268b</strong> has to be passed to this function and it has to return <strong>7</strong>. The return value will change after you edit the file.</li>

  </ul></li>

</ol>




<ol start="7">

 <li>Write a function named <strong>getNumberofAccounts</strong>. It accepts a string that stores the filename of a disk file and return an integer representing the number of accounts in the disk file.

  <ul>

   <li>Inside the function, open the file for reading using the filename passed to the function.</li>

   <li>Count the number of accounts in the file.</li>

   <li>For example, the file <strong>account_data</strong> has <strong>4</strong> Hence the name of the file <strong>account_data</strong> has to be passed to this function and it has to return 4. The return value will change after you edit the file.</li>

  </ul></li>

</ol>




<ol start="8">

 <li>Write a function named <strong>addAccount</strong>. It does not have any parameters.

  <ul>

   <li>Inside the function, open the <strong>account_data </strong>file for appending.</li>

   <li>Call the function getName to get the name of the new account.</li>

   <li>Call the function getNumber to get the number of the new account.</li>

   <li>Add the new account information to the data file in the same <strong>format (SEE SAMPLE OUTPUT)</strong>.</li>

  </ul></li>

 <li>Write a function named It accepts the account number to be removed.

  <ul>

   <li>Inside this function, call function <strong>getNumberofAccounts</strong> to get the current number of accounts in the data file <strong>account_data</strong>.</li>

   <li>Create a dynamic array of the structure type <strong>Account</strong>. Use the number of accounts in the data file for size of this dynamic array.</li>

   <li>Open <strong>dat</strong> file for reading.</li>

   <li>In a loop, read one line of the file at a time and store appropriate data in the dynamic array. Note that each element of the structure array will be an account available on a line of the file.

    <ul>

     <li>While reading check if the account number being read from the file matches the account number to be removed.</li>

     <li>If you find match, use a Boolean flag to store that you have found a match.</li>

     <li>Copy the entire file to your dynamic array whether or not you find a match.</li>

    </ul></li>

   <li>Close the file.</li>

   <li>If you have found a match while reading: o Open <strong>dat</strong> file for writing.

    <ul>

     <li>Write the contents of the dynamic array into the file, only if the account number does not match the account number to be removed.</li>

    </ul></li>

  </ul></li>

</ol>

If you have not found a match while reading:

<ul>

 <li>Notify the user with a suitable message to indicate the account number does not exist.</li>

</ul>

<ul>

 <li>Close the file.</li>

</ul>

<ol start="10">

 <li>Write a function named <strong>getCurrentBalance</strong>.

  <ul>

   <li>This function accepts two parameters: the account number and the type of account to get the balance of. The account type must be an enum data type.</li>

   <li>This function returns the current balance of the account being read.</li>

   <li>Inside the function, open the appropriate file for reading. For example, open the file <strong>145268b</strong> if the account number is <strong>145268</strong> and the account type is <strong>Business</strong>.</li>

   <li>Inside a loop, read the transactions in the file to find their sum.</li>

   <li>Return the computed sum representing the current account balance.</li>

  </ul></li>

 <li>Write a function named <strong>writeTransactions</strong>.

  <ul>

   <li>This function accepts two parameters: the account number and the type of account to get the balance of. The account type must be an enum data type.</li>

   <li>Inside the function, open the appropriate file for appending. For example, open the file <strong>145268b</strong> if the account number is <strong>145268</strong> and the account type is <strong>Business</strong>.</li>

   <li>Using a suitable message, ask the user for the transaction value.</li>

   <li>Write the transaction value to the appropriate file.</li>

  </ul></li>

</ol>




<ol start="12">

 <li>Write a function named <strong>displayAccount</strong>. It accepts the account number of the account to be display the transactions for. Inside this function: o Using a suitable message, ask the user which account needs to be displayed – Business or Personal. Use an integer variable for this purpose. o Using a suitable message, ask the user if the display needs to be sorted. Use a character variable for this purpose. o Inside the function, call the function <strong>getNumberofTransactions</strong> with appropriate arguments to get the number of transactions in the appropriate file. For example, if the account number is <strong>145268</strong> and the account type is <strong>Business</strong>, you must get the number of transactions from the file <strong>145268b.</strong> o Create a dynamic array of double type using the number of transactions in the file for the size of the array. You need an array since you may need to sort the transactions.

  <ul>

   <li>Inside the function, open the appropriate file for reading.</li>

   <li>Using a loop, read the content of the file one item at a time and store in your dynamic array.</li>

   <li>In a different loop, display the content of the array.

    <ul>

     <li>Your display must be sorted if the user has chosen to do so.</li>

     <li>Your numeric data must have two numbers after the decimal point.</li>

    </ul></li>

  </ul></li>

</ol>




<ol start="13">

 <li>Write a function named It accepts the account number of the account to process the transactions for. Inside this function:

  <ul>

   <li>Ask the user to choose which account the user wants to access – Business or Personal. Use a suitable integer value to get the choice from the user.</li>

   <li>Based on the choice of the user, design a switch case block to implement the following requirements.</li>

  </ul></li>

</ol>




<ul>

 <li>You must use the enumeration constants to set up your cases. o You must use a variable of your enumeration constant type for switching control.</li>

 <li>If the user chooses a Business account</li>

 <li>Call the function <strong>writeTransaction</strong> with appropriate arguments.</li>

 <li>Call the function <strong>getCurrentBalance</strong> with appropriate arguments. o If the user chooses a Personal account</li>

 <li>Call the function <strong>writeTransaction</strong> with appropriate arguments.</li>

 <li>Call the function <strong>getCurrentBalance</strong> with appropriate arguments.</li>

</ul>

o If the user enters a wrong choice, use the default case to provide an error message and ask the user to make the choice again.

➢ Your program needs to keep on asking the user for the choice until the user chooses a correct choice.

o Your numeric data must have two numbers after the decimal point.




<ul>

 <li>This function needs be able to process more than one transaction.</li>

</ul>

o After successfully processing a transaction, ask the user if the user wants to process another transaction.  o If the user chooses to process another transaction, use a suitable loop to ask the user about the type of account and the transaction to process.

<ol start="14">

 <li>Now that you’ve written and tested your program, make the following changes.

  <ul>

   <li>Create a file named <strong>cpp </strong>and copy the main function to this file.</li>

   <li>Create a file named <strong>cpp </strong>and copy all the functions (other than the main function) to this file.</li>

   <li>Create a file named <strong>cpp</strong> and copy all the global parameters as well as include fields and function headers to the header file. Make sure you include the header file in the .cpp files.</li>

   <li>Compile the files together and make sure it works correctly.</li>

   <li>You need to submit these three files to Canvas, where euid should be replaced by your EUID.</li>

  </ul></li>

</ol>




<ol start="15">

 <li>Your program will be graded based largely on whether it works correctly on the CSE machines (e.g., cse01, cse02, …, cse06), so you should make sure that your program compiles and runs on a CSE machine.</li>

</ol>







<strong>DESIGN (ALGORITHM): </strong>

On a piece of paper (or word processor), write down the algorithm, or sequence of steps, that you will use to solve the problem. You may think of this as a “recipe” for someone else to follow. Continue to refine your “recipe” until it is clear and deterministically solves the problem. Be sure to include the steps for prompting for input, performing calculations, and displaying output.

You should attempt to solve the problem by hand first (using a calculator as needed) to work out what the answer should be for a few sets of inputs.

Type these steps and calculations into a document (i.e., Word, text, or PDF) that will be submitted along with your source code. Note that if you do any work by hand, images (such as pictures) may be used, but they must be clear and easily readable. This document shall contain both the algorithm and any supporting hand-calculations you used in verifying your results.




<strong>Here are some sample outputs to help you write the code. The items in bold are entered by the user on the terminal as input data. </strong>

<strong> </strong>

<h2>SAMPLE OUTPUT 1</h2>

<strong> </strong>

$ ./a.out

+————————————————-


|          Computer Science and Engineering       |

|           CSCE 1030 – Computer Science I        |

|         Student Name EUID <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="e184948885a18c98cf948f95cf848594">[email protected]</a>       |

+————————————————-


<ol>

 <li>Add Account</li>

 <li>Remove Account</li>

 <li>Process Accounts</li>

 <li>Display Account Information</li>

 <li>Quit Enter your choice:<strong>1</strong></li>

</ol>

Enter your name:<strong>Firstname lastname </strong>

Enter your account number:<strong>123456</strong>

<ol>

 <li>Add Account</li>

 <li>Remove Account</li>

 <li>Process Accounts</li>

 <li>Display Account Information</li>

 <li>Quit Enter your choice:<strong>1</strong></li>

</ol>

Enter your name:<strong>newname newname</strong>

Enter your account number:<strong>456789</strong>

<ol>

 <li>Add Account</li>

 <li>Remove Account</li>

 <li>Process Accounts</li>

 <li>Display Account Information</li>

 <li>Quit Enter your choice:<strong>5</strong> Goodbye!!!</li>

</ol>




<h3>Screenshot of the account_data file after adding accounts</h3>










<h2>SAMPLE OUTPUT 2</h2>

$ ./a.out

+————————————————-


|          Computer Science and Engineering       |

|           CSCE 1030 – Computer Science I        |

|         Student Name EUID <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="e386968a87a38e9acd968d97cd868796">[email protected]</a>       |

+————————————————-


<ol>

 <li>Add Account</li>

 <li>Remove Account</li>

 <li>Process Accounts</li>

 <li>Display Account Information</li>

 <li>Quit Enter your choice:<strong>2</strong></li>

</ol>

Enter account number to remove:<strong>000000</strong>

Account does not exist.

<ol>

 <li>Add Account</li>

 <li>Remove Account</li>

 <li>Process Accounts</li>

 <li>Display Account Information</li>

 <li>Quit Enter your choice:<strong>2</strong></li>

</ol>

Enter account number to remove:<strong>123456</strong>

<ol>

 <li>Add Account</li>

 <li>Remove Account</li>

 <li>Process Accounts</li>

 <li>Display Account Information</li>

 <li>Quit Enter your choice:<strong>5</strong> Goodbye!!!</li>

</ol>

<h3>Screenshot of the account_data file after removing account number 123456</h3>







<strong> </strong>

<h2>SAMPLE OUTPUT 3</h2>

<strong> </strong>

$ ./a.out

+————————————————-


|          Computer Science and Engineering       |

|           CSCE 1030 – Computer Science I        |

|         Student Name EUID <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="e88d9d818ca88591c69d869cc68d8c9d">[email protected]</a>       |

+————————————————-


<ol>

 <li>Add Account</li>

 <li>Remove Account</li>

 <li>Process Accounts</li>

 <li>Display Account Information</li>

 <li>Quit Enter your choice:<strong>3</strong></li>

</ol>

Enter account number to process:<strong>145268</strong>

What is your account type?0 for Business, 1 for Personal:<strong>0</strong>

Enter transaction:<strong>15000</strong>

Business Balance:$44581.15

Do you want to process another transaction? Y/N:<strong>y</strong>

What is your account type?0 for Business, 1 for Personal:<strong>1</strong>

Enter transaction:<strong>5000</strong>

Personal Balance:$27999.75

Do you want to process another transaction? Y/N:<strong>n</strong>

<ol>

 <li>Add Account</li>

 <li>Remove Account</li>

 <li>Process Accounts</li>

 <li>Display Account Information</li>

 <li>Quit Enter your choice:<strong>5</strong> Goodbye!!!</li>

</ol>

<strong> </strong>

<h3>Screenshot of the 145268p file after entering transaction</h3>

<strong> </strong>




<h3>Screenshot of the 145268b file after entering transaction</h3>




<strong> </strong>

<strong> </strong>

<h2>SAMPLE OUTPUT 4</h2>




$ ./a.out

+————————————————-


|          Computer Science and Engineering       |

|           CSCE 1030 – Computer Science I        |

|         Student Name EUID <a href="/cdn-cgi/l/email-protection" class="__cf_email__" data-cfemail="eb8e9e828fab8692c59e859fc58e8f9e">[email protected]</a>       |

+————————————————-


<ol>

 <li>Add Account</li>

 <li>Remove Account</li>

 <li>Process Accounts</li>

 <li>Display Account Information</li>

 <li>Quit Enter your choice:<strong>4</strong></li>

</ol>

Enter account number:<strong>145268</strong>

Which account to display? 0 for Business, 1 for Personal:<strong>0</strong>

Do you want to sort? Y/N:<strong>n</strong>

12000.75

-3000.85

14500.50

2580.75 500.00

5000.00

-2000.00

<ol>

 <li>Add Account</li>

 <li>Remove Account</li>

 <li>Process Accounts</li>

 <li>Display Account Information</li>

 <li>Quit Enter your choice:<strong>4</strong></li>

</ol>

Enter account number:<strong>145268</strong>

Which account to display? 0 for Business, 1 for Personal:<strong>1</strong>

Do you want to sort? Y/N:<strong>y</strong>

10000.00

5000.00

5000.00

5000.00

3000.00

2000.00

1000.50

1000.00

-4000.75

-5000.00

<ol>

 <li>Add Account</li>

 <li>Remove Account</li>

 <li>Process Accounts</li>

 <li>Display Account Information</li>

 <li>Quit Enter your choice:<strong>5</strong> Goodbye!!!</li>

</ol>