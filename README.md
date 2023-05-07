Download Link: https://assignmentchef.com/product/solved-lab-exercise-5-problems
<br>
<ol>

 <li>Write C++ programs</li>

 <li>Compile C++ programs</li>

 <li>Implement programs that read and write to files</li>

</ol>

<h1><a id="user-content-instructions" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05#instructions" aria-hidden="true"></a>Instructions</h1>

Answer the programming problems sequentially (i.e., answer prob01 before prob02). If you have questions let your instructor or the lab assistant know. You can also consult your classmates.

When you answer two programming problems correctly, let your instructor know and wait for further instruction.

<h1><a id="user-content-lab-exercise-guide" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05#lab-exercise-guide" aria-hidden="true"></a>Lab exercise guide</h1>

Here’s a link to the <a href="https://docs.google.com/document/d/1EX01EtrO-pkHNLVPxiq7HNh1f5KnJZnr_dlJcO4T7t0/edit?usp=sharing" rel="nofollow">Lab exercise guide</a> in case you need to review the lab exercise objectives, grading scheme, or evaluation process.

<h1>Phonebook</h1>

This program is used to create a phonebook for storing contact information into a text file.

The program begins by asking the user to provide a name for the file that will contain their phone book information. It will then ask the user to provide the names and numbers of their contacts. It should keep asking the user for contact information until they type in <code>Done</code> (case-sensitive).

After the user types <code>Done</code>, store all contact information into the file name they provided at the beginning of the program. If the user does not add any contacts, then the file should be empty.

Please see the sample output below to guide the design of your program.

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob01#sample-output" aria-hidden="true"></a>Sample Output:</h2>

<pre>Please provide the file name for your phone book: <b>contacts.txt</b>Contact 1:Please provide the name: <b>Elsie Simon</b>Please provide their number: <b>(202)555-0115</b>Contact 2:Please provide the name: <b>Kaisha Cope</b>Please provide their number: <b>5455689016</b>Contact 3:Please provide the name: <b>Sultan Vargas</b>Please provide their number: <b>371-998-4166</b>Contact 4:Please provide the name: <b>Done</b>Saving phonebook into contacts.txtDone!</pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob01#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob01#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code save in <code>main.cpp</code> and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h5><code>make all</code></h5>




<h1>Phonebook display</h1>

This program loads contact information stored in a text file and displays it on the screen.

The program asks the user to provide the filename of a phonebook file. It will then load all of the names and numbers stored in the file and display them on the screen.

We assume that the file is stored using the correct format wherein for each contact, there is always a name followed by their phone number. Below is an example of a possible phonebook file.

<h2><a id="user-content-sample-phonebook-file-phonebooktxt" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob02#sample-phonebook-file-phonebooktxt" aria-hidden="true"></a>Sample phonebook file (phonebook.txt):</h2>

<pre><code>Shanay Wickens7205972770Harlee Collins3328206140Addison Ryan7917471622</code></pre>

Please see the sample output below assuming it loaded the phonebook file shown above to guide the design of your program. In case there are no contacts, inform the user that there were no contacts stored in the file. If the file does not exist, inform the user that the phonebook file is missing.

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob02#sample-output" aria-hidden="true"></a>Sample Output:</h2>

<pre>Please provide the file name for your phone book: <b>phonebook.txt</b>Contact 1:Name: Shanay WickensNumber: 7205972770Contact 2:Name: Harlee CollinsNumber: 3328206140Contact 3:Name: Addison RyanNumber: 7917471622</pre>

<h2><a id="user-content-empty-phonebook-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob02#empty-phonebook-sample-output" aria-hidden="true"></a>Empty phonebook sample Output:</h2>

<pre>Please provide the file name for your phone book: <b>phonebook.txt</b>Phone book does not contain any contacts!</pre>

<h2><a id="user-content-missing-phonebook-file-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob02#missing-phonebook-file-sample-output" aria-hidden="true"></a>Missing phonebook file sample Output:</h2>

<pre>Please provide the file name for your phone book: <b>phonebookszz.txt</b>Invalid phonebook file!</pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob02#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob02#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code save in <code>main.cpp</code> and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>

<h1>Donations</h1>

This program is used to store donor contributions into a text file.

The program begins by asking the user to provide the number of donors participating in their cause and then the name of the file to store donation information. It will then ask the user to provide the donation amounts for each of the donors. The number of donors and the donation amounts should be stored into the text file with the file name provided by the user.

The program should only store the file if the user indicates that there is at least one donor. Otherwise, the program will not ask for a filename and display an error.

Please see the sample output below to guide the design of your program.

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob03#sample-output" aria-hidden="true"></a>Sample Output:</h2>

<pre>Please provide the number of donors: <b>3</b>Please provide the name of the donations file: <b>donations.txt</b>Donor 1: $<b>35.00</b>Donor 2: $<b>500.00</b>Donor 3: $<b>235.10</b>Thank you for donating!</pre>

<h3><a id="user-content-sample-output-file" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob03#sample-output-file" aria-hidden="true"></a>Sample Output file:</h3>

<pre><code>335500235.10</code></pre>

<h2><a id="user-content-sample-invalid-input" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob03#sample-invalid-input" aria-hidden="true"></a>Sample invalid input:</h2>

<pre>Please provide the number of donors: <b>0</b>You need to have at least one donor for your cause to save donation information.</pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob03#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob03#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code save in <code>main.cpp</code> and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>




<h1>Donations display</h1>

This program loads donation information stored in a text file, displays each one on the screen, and displays the total donations.

The program asks the user to provide the filename of a donation file. It will then load all of the donations in the file and display them on the screen. Finally it will display the total of all donations.

A donation file’s first line describes the number of donations listed in the file followed by the donations. Below is an example of a possible donation file.

<h2><a id="user-content-sample-phonebook-file-donationstxt" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob04#sample-phonebook-file-donationstxt" aria-hidden="true"></a>Sample phonebook file (donations.txt):</h2>

<pre><code>4200143.23501.37396.88</code></pre>

Please see the sample output below assuming it loaded the donation file shown above to guide the design of your program. If the file does not exist, inform the user that the phonebook file is missing.

<h2><a id="user-content-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob04#sample-output" aria-hidden="true"></a>Sample Output:</h2>

<pre>Please provide the file name for your donation file: <b>donations.txt</b>Donation 1: $200.00Donation 2: $143.23Donation 3: $501.37Donation 4: $396.88Total donation: $1241.48</pre>

<h2><a id="user-content-missing-donation-file-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob04#missing-donation-file-sample-output" aria-hidden="true"></a>Missing donation file sample Output:</h2>

<pre>Please provide the file name for your donation file: <b>donationszz.txt</b>Invalid donation file!</pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob04#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob04#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code save in <code>main.cpp</code> and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<h6><code>make all</code></h6>

<h1>Consolidated report</h1>

This program loads a monthly report from a report file and displays the consolidated sales for a given range of months.

First, the program will ask the user to provide the filename of the monthly report file. Then the user will provide the number of months that will be consolidated and displayed. For example, if the user selects <code>1</code> then the total sales for each month will be shown. If the user selects <code>2</code> then every two months’ total sales will be added and shown. If the user selects <code>3</code> then the every three months’ total sales is shown and so on.

The program should only accept values equal to one or greater. Otherwise the program should display an error. If the number of months provided by the user does not perfectly divide the total number of months on the report, then it will just show the ranges that contain enough months. For example, if the user selects <code>2</code> and there are only 5 monthly reports, then it will display the total sales for months 1 and 2, and 3 and 4, only.

Below is an example of a possible monthly report file.

<h2><a id="user-content-sample-monthly-report-file-reporttxt" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob05#sample-monthly-report-file-reporttxt" aria-hidden="true"></a>Sample monthly report file (report.txt):</h2>

<pre><code>999.99705.67803.23400.54</code></pre>

Please see the sample output below assuming it loaded the report file shown above to guide the design of your program. If the file does not exist, inform the user that the report file is missing.

<h2><a id="user-content-sample-output---1-consolidated-month" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob05#sample-output---1-consolidated-month" aria-hidden="true"></a>Sample Output – 1 consolidated month:</h2>

<pre>Please provide the file name for your report file: <b>report.txt</b>Please provide the number of months to consolidate: <b>1</b>Month 1 sales: $999.99Month 2 sales: $705.67Month 3 sales: $803.23Month 4 sales: $400.54</pre>

<h2><a id="user-content-sample-output---2-consolidated-months" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob05#sample-output---2-consolidated-months" aria-hidden="true"></a>Sample Output – 2 consolidated months:</h2>

<pre>Please provide the file name for your report file: <b>report.txt</b>Please provide the number of months to consolidate: <b>2</b>Month 1 2 sales: $1705.66Month 3 4 sales: $1203.77</pre>

<h2><a id="user-content-sample-output---3-consolidated-months" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob05#sample-output---3-consolidated-months" aria-hidden="true"></a>Sample Output – 3 consolidated months:</h2>

<pre>Please provide the file name for your report file: <b>report.txt</b>Please provide the number of months to be consolidated: <b>3</b>Month 1 2 3 sales: $2508.89</pre>

<h2><a id="user-content-missing-report-file-sample-output" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob05#missing-report-file-sample-output" aria-hidden="true"></a>Missing report file sample Output:</h2>

<pre>Please provide the file name for your report file: <b>reportszz.txt</b>Invalid report file!</pre>

<h1><a id="user-content-submission-checklist" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob05#submission-checklist" aria-hidden="true"></a>Submission checklist</h1>

<ol>

 <li>Compiled and ran the driver (<code>main</code>).</li>

 <li>Manually checked for compilation and logical errors.</li>

 <li>Ensured no errors on the unit test (<code>make test</code>).</li>

 <li>Followed advice from the stylechecker (<code>make stylecheck</code>).</li>

 <li>Followed advice from the formatchecker to improve code readbility (<code>make formatcheck</code>).</li>

</ol>

<h1><a id="user-content-code-evaluation" class="anchor" href="https://github.com/peskin55/CPSC121/tree/master/Labs/Lab_05/prob05#code-evaluation" aria-hidden="true"></a>Code evaluation</h1>

Open the terminal and navigate to the folder that contains this exercise. Assuming you have pulled the code inside of <code>/home/student/labex02-tuffy</code> and you are currently in <code>/home/student</code> you can issue the following commands

<pre><code>cd labex02-tuffy</code></pre>

You also need to navigate into the problem you want to answer. To access the files needed to answer problem 1, for example, you need to issue the following command.

<pre><code>cd prob01</code></pre>

When you want to answer another problem, you need to go back up to the parent folder and navigate into the next problem. Assuming you are currently in <code>prob01</code>, you can issue the following commands to go to the parent folder then go into another problem you want to answer; <code>prob02</code> for example.

<pre><code>cd ..cd prob02</code></pre>

Use the <code>clang++</code> command to compile your code and the <code>./</code> command to run it. The sample code below shows how you would compile code save in <code>main.cpp</code> and into the executable file <code>main</code>. Make sure you use the correct filenames required in this problem. Take note that if you make any changes to your code, you will need to compile it first before you see changes when running it.

<pre><code>clang++ -std=c++17 main.cpp -o main./main</code></pre>

You can run one, two, or all the commands below to <code>test</code> your code, <code>stylecheck</code> your code’s design, or <code>formatcheck</code> your work. Kindly make sure that you have compiled and executed your code before issuing any of the commands below to avoid errors.

<pre><code>make testmake stylecheckmake formatcheck</code></pre>

A faster way of running all these tests uses the <code>all</code> parameter.

<pre><code>make all</code></pre>