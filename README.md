Download Link: https://assignmentchef.com/product/solved-cs2102-homework-2-abstract-classes-and-programming-with-lists
<br>



<h1>Assignment Goals</h1>

To be able to share data/code among classes using abstract classes

To use the Java LinkedList class

To become familiar with element-based for loops

<h1>Reminders</h1>

<strong> Please use the default package in your Java project.</strong> There will be a penalty for using a named package.

Starting with this assignment, please include a Javadoc statemnt above each method. There will be a penalty for forgetting your Javadoc statements.

<a href="https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html"><strong>LinkedList API:</strong></a> <a href="https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html"><strong>https://docs.oracle.com/</strong></a><a href="https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html"><strong>j</strong></a><a href="https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html"><strong>avase/8/docs/api/</strong></a><a href="https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html"><strong>j</strong></a><a href="https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html"><strong>ava/util/LinkedList.html</strong></a>

<a href="https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html"><strong>(https://docs.oracle.com/</strong></a><a href="https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html"><strong>j</strong></a><a href="https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html"><strong>avase/8/docs/api/</strong></a><a href="https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html"><strong>j</strong></a><a href="https://docs.oracle.com/javase/8/docs/api/java/util/LinkedList.html"><strong>ava/util/LinkedList.html)</strong></a>

<strong>Note to those with prior Java experience:</strong> One goal of 2102 is to help everyone learn when different iteration constructs (for, while, etc) are needed for a particular problem. Style grading will check whether you are using appropriate constructs. This week, we will cover the per-element style for loop, not the for loop that uses a variable to index into elements. For full points, do not use index-based for loops on this assignment. Use a per-element style loop instead.

We will have covered the material for this assignment during the second week of classes.

<h1>Problem Description and Context</h1>

For last week’s homework, you developed classes for contestants and matches. Now we want to build off of those to create <em>tournaments. </em>A tournament is a set of <em>rounds</em>, each of which in turn consists of a set of <em>matches. </em>

There are two kinds of rounds: <em>initial</em> rounds occur at the beginning of the tournament (like how every team plays at least three games in the FIFA World Cup); <em>advanced</em> rounds occur later in the tournament and involve contestants who advanced from earlier matches in the tournament (such as the quarterfinals, semi-finals, and finals in the World Cup).

We are going to capture tournaments in Java in a way that reuses the classes and interfaces you created for homework 1 (you are welcome to update or fix your work from homework 1 as needed).

<h1>Programming Problems</h1>

<ol>

 <li>Starting with your Homework 1 submission, develop an additional set of classes and interfaces that capture the concepts of rounds and tournaments. In order to let us run tests against your code, everyone needs to use standard names for interfaces and classes. Use the following:</li>

</ol>

InitRound , AdvancedRound , and AbsRound for rounds

Tournament for the tournament class

Also create an interface IWinner for reasons that will be explained farther down.

The class constructor signatures should look like the following (parameter names may vary, of course):

<ol start="3">

 <li>Both InitRound and AdvancedRound have a method getMatchWinners() that returns a LinkedList of all of the <em>contestants</em> that won each match in each round.</li>

 <li>Both InitRound and AdvancedRound have a method getNumWinners() that returns the number of winners in the round. Think about how you could use the a call to the getMatchWinners() method in this method.</li>

 <li>AdvancedRound has a method isWinner() that takes in an IContestant and returns whether that contestant was one of the winners from the previous round. This makes sure that there is nobody advancing who shouldn’t be advancing.</li>

 <li>InitRound also has a method isWinner() that takes in an IContestant and determines whether that contestant is a winner by checking to see that the contestant was a winner in at least one of the matches that makes up that round.</li>

 <li>AbsRound is an abstract class that holds fields and method implementations common to both</li>

</ol>

InitRound and AdvancedRound

<ol start="8">

 <li>Tournament has a single LinkedList of all of the rounds (both initial and advanced) that make up the tournament.</li>

 <li>Tournament has a method finalWinnerIsValid() that takes in a contestant representing the tournament winner and checks whether that contestant is a valid winner. A contestant is a valid winner if he or she has won at least half of the rounds in the tournament. Use the isWinner() methods in InitRound and AdvancedRound and the IWinner interface to solve this problem.</li>

 <li>Create a test suite for your work. Put all of your tests and test data in a class called Examples . <strong><em>Your class must be called this so that the auto-grader can find it!</em></strong></li>

</ol>

<strong><em>Just because your program passes all of your JUnit tests does not guarantee that it will pass all of ours.</em></strong> However, you can minimize the risk that your methods will fail our JUnit tests by sticking with the proper naming conventions and writing as many edge cases as possible. The more testing you do, the less the likelihood of failure!

<h1>Support Files</h1>

Here are a couple of files that may be helpful.

<a href="https://canvas.wpi.edu/courses/16466/files/2217271/download?download_frd=1">a skeletal </a><a href="https://canvas.wpi.edu/courses/16466/files/2217271/download?download_frd=1"><strong>Examples.</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217271/download?download_frd=1"><strong>j</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217271/download?download_frd=1"><strong>ava</strong></a> <a href="https://canvas.wpi.edu/courses/16466/files/2217271/download?download_frd=1"><strong> </strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217271/download?download_frd=1"><strong>(https://canvas.wpi.edu/courses/16466/files/2217271/download?</strong></a>

<a href="https://canvas.wpi.edu/courses/16466/files/2217271/download?download_frd=1"><strong>download_frd=1) </strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2217271/download?download_frd=1">file showing you the shape of a test case. You should create your own</a>

Examples.java file by right-clicking your project in Eclipse and going to New -&gt; JUnit Test Case.

<strong>Make sure JUnit 4 is selected!</strong>

<a href="https://canvas.wpi.edu/courses/16466/files/2261339/download?download_frd=1">a </a><a href="https://canvas.wpi.edu/courses/16466/files/2261339/download?download_frd=1"><strong>CompileCheck.</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2261339/download?download_frd=1"><strong>j</strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2261339/download?download_frd=1"><strong>ava</strong></a> <a href="https://canvas.wpi.edu/courses/16466/files/2261339/download?download_frd=1"><strong> </strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2261339/download?download_frd=1"><strong>(https://canvas.wpi.edu/courses/16466/files/2261339/download?</strong></a>

<a href="https://canvas.wpi.edu/courses/16466/files/2261339/download?download_frd=1"><strong>download_frd=1) </strong></a><a href="https://canvas.wpi.edu/courses/16466/files/2261339/download?download_frd=1">file that attempts to create objects from the expected classes and call th</a>e expected methods within those classes. Including this file when you compile will check that you have the class and method names that our grading tools expect, which saves you from losing points.

If you get a compilation error involving this file on a class or method that you defined, <strong>do not edit this file. Edit your files instead!</strong> As you are working, you may wish to comment out sections of the file that check methods you haven’t written yet (that’s fine). The final work you turn in should, however, compile against the entire contents of this file.

<strong><em>Just because your programs compiles does not mean that your program will pass all of the auto-grader tests!</em></strong> A program can compile but still be full of errors. The CompileCheck file is there only to make sure your naming conventions are correct, not that your classes and methods work correctly.

You are welcome to leave this file in the directory when you submit your work. It can serve as the main method for your program.


