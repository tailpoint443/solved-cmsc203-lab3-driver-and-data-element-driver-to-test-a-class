Download Link: https://assignmentchef.com/product/solved-cmsc203-lab3-driver-and-data-element-driver-to-test-a-class
<br>
<strong style="font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, Oxygen-Sans, Ubuntu, Cantarell, 'Helvetica Neue', sans-serif;">Lab Objectives</strong>




<ul>

 <li>Write a Java program from pseudo-code</li>

 <li>Write a driver program to test a separate class</li>

 <li>Create an object from a class’s constructor</li>

 <li>Write a loop to repeat a task</li>

</ul>







<strong>Introduction</strong>







In this lab, you are introduced to multiple classes (a driver class and a data element class).  You will write the driver class in order to test the various methods provided in the data element class.




You are given a file called Movie.java, which has the data fields for a movie, along with “setters” and “getters”, and a “toString” method.  You will create a driver class from the pseudocode in Task #1 below to test the Movie class.




Follow the directions exactly, and in order.




<strong>Task #0 Review the Movie Class</strong>




<ol>

 <li>Copy the file Movie.java (see code listing 3.1) from Blackboard.</li>

 <li>Create a project in Eclipse and import Movie.java.</li>

 <li>Open Movie.java and observe the three data fields (attributes). Notice that the fields are declared as private, so they are not accessible outside the class. They are accessed via public setter and getter methods and in general any public method defined within the class Movie. (This is called “data hiding”, a part of “encapsulation”, and a good programming practice).  There is also a method in Movie called toString(), which prints out the information for a movie.</li>

 <li><strong>NOTE</strong>: You should not modify Movie.java.</li>

</ol>




<strong>Task #1 Writing a Driver Class</strong>




<ol>

 <li>Create a new class called MovieDriver. In Eclipse, right-click on the project you created and select New-&gt;Class.  In the wizard, name the class MovieDriver and check the box to create a main method.</li>

 <li>Open the file MovieDriver.java in Eclipse. Write Java code to implement the following pseudocode:</li>

</ol>

<em>Create a new object of type Scanner that reads from the keyboard</em>

<em>Create a new movie object</em>

<em>Prompt the user to enter the title of a movie </em>

<em>Read in the line that the user types</em>

<em>Set the title in the movie object</em>

<em>Prompt the user to enter the movie’s rating</em>

<em>Read in the line that the user types</em>

<em>Set the rating in the movie object</em>

<em>Prompt the user to enter the number of tickets sold at a (unnamed) theater</em>

<em>Read in the integer that the user types</em>

<em>Set the number of tickets sold in the movie object</em>

<em>Print out the information using the movie’s toString method</em>

<em> </em>

<ol start="3">

 <li>Run your driver class to be sure it prints out the information you type in.</li>

 <li>Your Eclipse console should look something like this:</li>

</ol>




<strong>Task #2 Writing a Loop</strong>

<ol>

 <li>Add to your driver class a loop that reads input for multiple movies. Your code does <u>not</u> need to save each movie as you enter the next one.</li>

 <li>Ask the user if they want to continue, and continue the loop if the user types the correct response.</li>

 <li>Run the new driver to ensure that it reads and prints multiple movies.</li>

 <li>Your Eclipse console should look something like this:</li>

 <li>HINT: if your program ends before reading your keyboard input, you may have not read the previous line feed, so when you read a line expecting it to be the next line of input, it is instead just the previous “
”. To solve this problem, you may be able to put in an additional nextLine(); just to read and discard the line feed.;where keyboard is an object of the scanner class.</li>

</ol>

<strong> </strong>

<strong> </strong>

<strong>Task #3 – Upload your java files to GitHub</strong>




Upload your java files to GitHub in a directory named CMSC203_Lab3.







<strong>Turn in the following:</strong>

MovieDriver.java from Task #2 and Movie.java (<strong>NOT the .class files</strong>; submit the .java files).  Submit both files, even though you have not changed Movie.java.




<strong>Code Listing 3.1 – Movie.java</strong>




public class Movie {




private String title;

private String rating;

private int  soldTickets;







public  Movie ()

{

title = “”;

rating = “”;

soldTickets = 0;

}




public  Movie (Movie m)

{

title = m.title;

rating = m.rating;

soldTickets = m.soldTickets;

}




public Movie(String title, String rating, int soldTickets) {




this.title = title;

this.rating = rating;

this.soldTickets = soldTickets;

}




public String getTitle() {

return title;

}




public void setTitle(String title) {

this.title = title;

}




public String getRating() {

return rating;

}




public void setRating(String rating) {

this.rating = rating;

}




public int getSoldTickets() {

return soldTickets;

}




public void setSoldTickets(int soldTickets) {

this.soldTickets = soldTickets;

}




public String toString() {

return (this.title+” (“+this.rating+”): Tickets Sold: “+this.soldTickets);

}

}


