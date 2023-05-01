Download Link: https://assignmentchef.com/product/solved-bbm104-assignment-2-calorie-calculation
<br>
In this experiment you are expected to gain knowledge on basic JAVA programming. The program you are going to develop will deal with variables, loops, string operations, file read and write operations. Besides the programming task, you will also learn to comply with coding standards.

1. Problem Definition

In this experiment you are expected to write Java code that calculates the calories by considering taken and burned calories during the day for the healthy life of the people. You will be given three text files as follows:

1.1 Text for information of people (people.txt)

This text file includes personal information of each person, which are person ID <strong>(personID)</strong>, name <strong>(name)</strong>, gender <strong>(gender)</strong>, weight <strong>(weight), </strong>height<strong> (height) </strong>and date of birth <strong>(dateOfBirth) </strong>as shown in following table. Every item in the file separated with a <strong>tab</strong> character. This text file contains up to 50 items.

<strong>[person ID]</strong> <em>tab</em> <strong>[name]</strong> <em>tab</em> <strong>[gender]</strong> <em>tab</em> <strong>[weight]</strong> <em>tab </em><strong>[height]</strong><em> tab </em><strong>[date of birth]</strong><em> newline </em>

<strong>[person ID] </strong><em>tab </em><strong>[name] </strong><em>tab </em><strong>[gender] </strong><em>tab </em><strong>[weight] </strong><em>tab </em><strong>[height] </strong><em>tab </em><strong>[date of birth] </strong><em>newline </em>

<h2>Example content of people.txt</h2>

<table width="0">

 <tbody>

  <tr>

   <td width="55">12345</td>

   <td width="48">ahmet</td>

   <td width="96">male       78</td>

   <td width="48">175</td>

   <td width="379">1987</td>

  </tr>

  <tr>

   <td width="55">12346</td>

   <td width="48">ahmet</td>

   <td width="96">male       92</td>

   <td width="48">189</td>

   <td width="379">1990</td>

  </tr>

  <tr>

   <td width="55">12378 ……..</td>

   <td width="48">gizem</td>

   <td width="96">female 61</td>

   <td width="48">172</td>

   <td width="379">1986</td>

  </tr>

 </tbody>

</table>




<h3>1.2 Text for food (food.txt)</h3>

This text file includes information of foods, which are food ID <strong>(foodID)</strong>, name of food <strong>(nameOfFood)</strong> and calorie count <strong>(calorieCount) </strong>as shown in the following table. Every item in the file separated with a <strong>tab</strong> character.  For each food, 1 portion is 100 grams and the calorie count in the table is calculated for 1 portion. ID of fruits groups start with 10.., ID of meal groups start with 11.., ID of dessert groups start with 12.. and they consist of a 4-digit number. This text file contains up to 100 items.

<strong>[food ID]</strong> <em>tab</em> <strong>[name of food]</strong> <em>tab</em> <strong>[calorie count]</strong> <em>newline </em>

<strong>[food ID] </strong><em>tab </em><strong>[name of food] </strong><em>tab </em><strong>[calorie count] </strong><em>newline </em>

<strong> </strong>

<h2>Example content of food.txt</h2>

1001       apple          57

<ul>

 <li>spaghetti 131</li>

 <li>lahmacun 185</li>

</ul>

……

1201       baklava       521

…….

<strong> </strong>

<h3>1.3 Text for sport activities (sport.txt)</h3>

This text file includes information of sport, which are sport ID <strong>(sportID)</strong>, name of sport<strong> (nameOfSport)</strong> and calorie burned <strong>(calorieBurned) </strong>as shown in the following table. Every item in the file separated with a <strong>tab</strong> character. The calories burned for each sport are calculated for 60 minutes. ID of sport activities start with 20.. and they consist of a 4-digit number. This text file contains up to 100 items.

<strong>[sport ID]</strong> <em>tab</em> <strong>[name of </strong><strong>sport</strong><strong>]</strong> <em>tab</em> <strong>[calorie burned]</strong> <em>newline </em>

<strong>[sport ID] </strong><em>tab </em><strong>[name of </strong> <strong>sport ] </strong><em>tab </em><strong>[calorie burned] </strong><em>newline </em>




<h2>Example content of sport.txt</h2>

<ul>

 <li>swimming 400</li>

 <li>running              300</li>

</ul>

…..

2013       tennis                   275

……

<strong> </strong>

<h1>2. Calculation of daily calorie needs</h1>

The daily calorie needs <strong>(dailyCalorieNeeds)</strong> of people vary by gender, age, height and weight. Therefore, it will be calculated separately for men and women as follows:




The daily calorie needs <strong>(dailyCalorieNeeds)</strong> should always be rounded to the closest integer value.

<h1>3. Text for input (command.txt)</h1>

Each line of the input file named as command.txt consists of either person ID <strong>(personID)</strong>, food ID <strong>(foodID)</strong> and the number of portions <strong>(numberOfPortion),</strong> or person ID <strong>(personID)</strong>, sport ID<strong> (sportID)</strong> and sport duration <strong>(sportDuration) </strong>as shown in the table below<strong>. </strong>During day, a person may add food ID that is eaten and sport ID that is done into this file. The <strong>print(personID)</strong> command should write the current calorie status of the specified person in command.txt file to monitoring.txt file. The <strong>printList</strong> command should write calorie statuses of all people given in command.txt file to monitoring.txt file. The expected output format is given in section 4.

<table width="0">

 <tbody>

  <tr>

   <td width="627"><strong>[person ID]</strong> <em>tab</em> <strong>[food ID]</strong> <em>tab</em> <strong>[number of portions]</strong> <em>newline </em><strong>[person ID] </strong><em>tab </em><strong>[sport ID] </strong><em>tab </em><strong>[sport duration] </strong><em>newline </em><em>….. </em><strong>print(personID)</strong><em> newline </em><strong>[person ID] </strong><em>tab </em><strong>[sport ID] </strong><em>tab </em><strong>[sport duration] </strong><em>newline </em><strong>printList</strong><em> newline ….. </em></td>

  </tr>

 </tbody>

</table>




<strong><em>Example content of command.txt </em></strong>

12345    1001       2

12378     1002      3

…..

print(12345)

12345    2001       45

12378 1001       1 printList

<strong><em>……</em></strong>




<h1>4. Text for output (monitoring.txt)</h1>

You are expected to write output of your program to a text file named as monitoring.txt for persons specified in command.txt file.  This text file should include the following information for each person in order as shown in the following table: name <strong>(name)</strong>, age <strong>(age)</strong>, daily calorie needs <strong>(dailyCalorieNeeds),</strong> calories taken <strong>(caloriesTaken)</strong>, calories burned <strong>(caloriesBurned</strong>) and result <strong>(result) </strong>for print (personID) and printList. If the result is a number less than zero, it means that a person has taken less calories than they should take during a day. On the other hand, if the result is greater than zero, a person has taken more calories than they should take during a day. Daily calorie needs <strong>(dailyCalorieNeeds), </strong>calories taken<strong> (caloriesTaken) </strong>and calories burned<strong> (caloriesBurned)</strong> should always be rounded to the closest integer value. Therefore, the result (<strong>result</strong>) will automatically be an integer. Also, the output file should include <strong>person ID (personID), </strong>calories taken, name of food<strong> (nameOfFood)</strong>, calories burned and name of sport <strong>(nameOfSport)</strong> to keep track calories burned and taken for a given person in input file. <strong> </strong>Every item in the file separated with a <strong>tab</strong> character

<strong>[person ID] </strong><em>tab </em><strong>has </strong><em>tab</em><strong> taken </strong><em>tab</em><strong> [calories taken]kcal </strong><em>tab</em><strong> from </strong><em>tab</em><strong> [name of food]</strong><em> newline </em>

<em>*************** (There will be 15 stars ) newline </em>

<strong>[person ID] </strong><em>tab </em><strong>has </strong><em>tab </em><strong>burned </strong><em>tab </em><strong>[calories burned]kcal</strong><em> tab </em><strong>thank </strong><em>tab </em><strong>to </strong><em>tab </em><strong>[name of sport]</strong><em> newline </em>

<em>*************** (There will be 15 stars ) newline </em>

<strong>[name] </strong><em>tab </em><strong>[age] </strong><em>tab </em><strong>[daily calorie needs] </strong><em>tab </em><strong>[calories taken] </strong><em>tab </em><strong>[calories burned] </strong><em>tab </em><strong>[result] </strong><em>newline </em>

<em>*************** (There will be 15 stars ) newline </em>

<strong>[name] </strong><em>tab </em><strong>[age] </strong><em>tab </em><strong>[daily calorie needs] </strong><em>tab </em><strong>[calories taken] </strong><em>tab </em><strong>[calories burned] </strong><em>tab </em><strong>[result] </strong><em>newline *************** (There will be 15 stars ) newline </em>

<em>…….. </em>







<strong><em>Example content of monitoring.txt</em></strong>

<table width="0">

 <tbody>

  <tr>

   <td colspan="2" width="295">12345    has taken 200kcal from apple***************12356   has burned 100kcal thanks to tennis***************ahmet       27           1897kcal               2300kcal</td>

   <td width="331">400kcal     +3kcal</td>

  </tr>

  <tr>

   <td width="199">***************ahmet       27           1897kcal</td>

   <td width="96">2300kcal</td>

   <td width="331">400kcal     +3kcal</td>

  </tr>

  <tr>

   <td width="199">gizem        25           1789kcal*************** ……..</td>

   <td width="96">1900kcal</td>

   <td width="331">430kcal    -319kcal</td>

  </tr>

 </tbody>

</table>




<h1>5. Example content of input and output file</h1>

In this experiment, you will be given an input file (command.txt) as below and you are expected to create an output file as shown below (monitoring.txt) by considering this given input file. The values in the example content of files given above (section 1.1, 1.2 and 1.3) are taken into consideration in this input and output files.

<h2>command.txt</h2>

12345    1102       4

12378     1101      3 print (12345)

12345    2001       45

printList

12378   1001         1




<h2>monitoring.txt</h2>

12345    has taken  740kcal  from  lahmacun

***************

12378   has taken 393kcal  from  spaghetti

***************

ahmet     31    1803kcal      740kcal 0kcal           -1063kcal

***************

12345 has burned 300kcal thanks to swimming

***************

ahmet  31  1803kcal   740kcal     300kcal         -1363kcal gizem            32   1393kcal   393kcal  0kcal                  -1000kcal

***************

12378 has taken  57kcal  from  apple