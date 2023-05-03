Download Link: https://assignmentchef.com/product/solved-cs1027-lab1
<br>
<h1>Learning Outcomes</h1>

<ul>

 <li>Create a custom class with relevant instance variables</li>

 <li>Add a constructor and getter and setter methods to a class</li>

 <li>Instantiate objects of a custom class</li>

 <li>Identify when and how to add toString() and equals() methods to a class  Document code thoroughly to generate clear Javadocs</li>

</ul>

<h1>Pre-Lab</h1>

Read the <a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab01/javadoc.html">Javadoc explanation</a><a href="https://www.csd.uwo.ca/courses/CS1027a/labs/lab01/javadoc.html">.</a>

Question: What information is needed in a method’s javadoc? What tags will you need to use?

<h1>Exercise 1 – Develop a custom class</h1>




<ol>

 <li>Create a new Project (select File &gt; New &gt; Java Project) and name it: Lab1</li>

 <li>Within this project, add a new class and name it: Player</li>

 <li>This class will represent hockey players, so it should have three private instance variables: name (of type String), position (String), and jerseyNum (int)</li>

 <li>Add a constructor that takes in three parameters to match the instance variables (i.e. same names and types).</li>

 <li>In this constructor, assign each of the instance variables with the corresponding input parameter. You must use “this.” before assigning them since the names are the same.</li>

</ol>

Question: Why do we need to use the “this” keyword? What happens if we don’t use it?

<ol start="6">

 <li>Below the constructor, add a getter method called getName that returns the player’s name. Note that the return type “String” must be included in the method signature.</li>

 <li>Add two more getter methods, getPosition and getJerseyNum, that return the corresponding variable values.</li>

 <li>After the three getter methods, add a setter method called setName that takes in a String variable called newName and assigns that input parameter’s value into the name.</li>

</ol>

Note that the return type should be void since nothing has to be returned.

<ol start="9">

 <li>Follow this setter method with two more setters: setPosition and setJerseyNum</li>

 <li>At this point, your Player.java class should have three private instance variables at the top, a constructor, three getters, and three setters.</li>

</ol>

<h1>Exercise 2 – Test the class methods</h1>

<ol>

 <li>Inside the Lab1 project, add another class with the name TestLab and add a main method (either by checking the “method stub” checkbox in the New Class window or by typing the method signature manually).</li>

 <li>In the main method, create a new Player variable called p1 and instantiate it as a new Player object. Use your name for the player’s name, and use any value for position (i.e. “defence”) and jerseyNum.</li>

 <li>Add three print lines: one to print getName(), one for p1.getPosition(), and one for p1.getJerseyNum().</li>

 <li>Save and run the file. The values you used for the player will be printed to the console.</li>

 <li>Use each of the setters to change your name, position, and jersey number.</li>

 <li>Copy the print lines with the getters from above and paste them after using the setters.</li>

 <li>Save and run the file. You should now see the updated values, which were just changed from the setters, printed to the console.</li>

 <li>Add a print line with just p1 in the parentheses (i.e. printing the object itself, not a specific variable retrieved from a getter).</li>

 <li>Save and run the file. The bottom print line looks like gobbledygook! This is the default format of printing out an object; it starts with the class name followed by a sequence of characters. In the next exercise, you will add a toString() method which overrides this default format for printing.</li>

 <li>Create another Player object called p2 and instantiate it with the values that you used in the setters (i.e. the updated p1 values and p2’s default values should be the same).</li>

 <li>Add the following lines of code to compare the two objects: if (p1.equals(p2)) {</li>

</ol>

System.out.println(“Same player”);

} else {

System.out.println(“Different player”);

}




Question: Which of these lines do you expect to print out?




<ol start="12">

 <li>Save and run the file. Was your prediction correct?</li>

 <li>Much like the toString() method, there is a default equals() method that you can override to control the way comparisons are made between two objects of your class.</li>

</ol>




<h1>Exercise 3 – Adding toString() and equals() methods</h1>




<ol>

 <li>Go back into the Player file.</li>

 <li>Near the bottom (after your getters and setters), add a toString method that is public and has a String return type. Within this toString() method, type:</li>

</ol>

return this.name + “:  #” + this.jerseyNum;

<ol start="3">

 <li>Go back to the TestLab file and run it. The print line of the object p1 should now display relevant information from the object in the format specified in toString() rather than the sequence of characters it showed before.</li>

 <li>Go back again to the Player class.</li>

 <li>After the toString() method, add a method called equals that is public and has a boolean return type. This method must take in a single parameter of type Player and we’ll call it “other” for simplicity.</li>

 <li>In the equals method, add a conditional that checks if this.name.equals(other.name) and if it does, return true. If not, return false.</li>

</ol>




Question: Which class contains the equals() method being called here? Is it calling itself?




<ol start="7">

 <li>The problem with this equals method currently is that two players who happen to have the same name would be considered the same person which is not correct. Adapt the conditional to return true if the names are equal AND the jersey numbers are equal (HINT: use &amp;&amp; for an AND operator, and use == when comparing numbers). This still might not be a perfect way of comparing players (i.e. consider two different people named John who each wear #25 on their respective teams) but it’s sufficient for this exercise.</li>

 <li>Save the file. Go back to TestLab and run it.</li>

 <li>Experiment by changing one of the names and/or positions to test the equals() method with various cases.</li>

</ol>




<h1>Exercise 4 – Writing comments and generating Javadocs</h1>




<ol>

 <li>Go into the Player class.</li>

 <li>In the method getName(), add a single line comment (//) just above the return statement.</li>

</ol>

The lines in this method should now look like this.

<table width="221">

 <tbody>

  <tr>

   <td colspan="2" width="221">// Get the player’s name.</td>

  </tr>

  <tr>

   <td width="106">return name;</td>

   <td width="115"> </td>

  </tr>

 </tbody>

</table>

<ol start="3">

 <li>In the constructor, add a few empty lines at the top before initializing the variables.</li>

 <li>Add a multi-line comment in that space by starting with /* and ending on another line with */</li>

 <li>Add some descriptive text within this comment section. For example,</li>

</ol>

/*

This is the constructor so we will be

initializing the member variables here */

<ol start="6">

 <li>Refer back to the pre-lab reading, which you should have read before starting, to review how Javadoc comments are formatted.</li>

 <li>Add Javadoc comments to class Player to explain purpose and author of the class, purpose, parameter, and return value of the methods (you can just do it for the constructor, one of the getters, and one of the setters to see how it works).</li>

 <li>Click on Project &gt; Generate Javadoc…</li>

 <li>For the Javadoc command, click on the Configure button, locate the “javadoc” program and click “Open”. This program will be in the “bin” directory of the Java Development Kit</li>

</ol>

installation on the machine. This could for instance be C:Program FilesJavajdk1.8.0_03binjavadoc.exe

<ol start="10">

 <li>Select the project “Lab1” for which you want to generate the documentation.</li>

 <li>Ensure that Public and Use Standard Doclet are selected and click Finish.</li>

 <li>Javadoc generates a set of html files which comprise the documentation for the program. You should see these in the Package Explorer in Eclipse inside “Lab1” under the “doc” directory. You can view any of the html files by selecting “doc” and then double clicking on an html file (start with index.html).</li>

</ol>


