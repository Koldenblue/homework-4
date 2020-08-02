# JavaScript Quiz Questions

There are two objectives for this project: the first objective is to demonstrate a framework for creating a simple quiz website. The second objective, of course, is to provide a short JavaScript quiz.

The quiz website itself can be accessed at https://koldenblue.github.io/quiz-template/


![image](https://user-images.githubusercontent.com/64618290/89129919-07e7f580-d4b6-11ea-9079-0398cf746e5a.png)


![image](https://user-images.githubusercontent.com/64618290/89129938-306fef80-d4b6-11ea-830a-af0df785886e.png)
<br>
<br>

## A Template for Quizzes

The quiz and high score functions of the website are all performed without ever necessitating a page reload. Instead, the main body of the quiz and high scores are all created and displayed using JavaScript. A key advantage to this is that the JavaScript code, along with the accompanying HTML containers in the &gt;body&lt; of the HTML, can be ported to other websites. Styling and placement using CSS would still be necessary, of course, and namespace collisions would have to be checked for. Some of the styling is done using Bootstrap, and so Bootstrap script tags would have to be added as well. With that in mind, I believe that this code could be used as part of a more complex website.

### JavaScript Code Discussion
There are four main parts to the JavaScript code. But first, the actual questions can be edited to pertain to any topic, of course. The page title and header in the html ("Coding Quiz") can be changed as well.

The main functions at the top are responsible for initializing the layout and controlling the actual running of the quiz. 

Next, the timer functions simply display the quiz time and penalize the user for incorrect answers. The time for the quiz also functions as the user's score at the end of the quiz. The quiz time, as well as the penalty time, can be changed using the TOTALTIMEGIVEN and PENALTYTIME constants near the top of the code. These constants should be changed depending on the number of questions and desired scoring difficulty.

Third, the quiz layout functions are responsible for actually displaying the questions and answers. As one of the questions points out, one weakness in this code is that the correct answers can simply be found by looking at the DOM, or at the JavaScript code itself. The quiz layout functions create a new container for each question and answer and append them to the page. Therefore, a question can have as many or as few answers as desired.

Finally, the high score functions accept user names as input. Then, the names and associated scores are displayed in the high score list, sorted by score in descending order. These names and score numbers are only stored locally. Name validation is simply designed to accept between 1 and 50 characters of any type. The maximum name length can be changed by editing the MAXNAMELENGTH constant. The program is designed to only accept the top 10 scores, but this can be changed by editing the SCORELISTLENGTH constant. The top 10 scores are sorted with a bubble sort algorithm. If it is desired to keep track of a significantly larger number of high scores, the program could also be improved by adding in a more efficient sorting algorithm, such as a merge sort or quick sort.

### Goals and Results
Overall, the goal of this webpage was to provide a template for simple quizzes that can be given in a web browser. This goal was accomplished almost entirely through DOM manipulation by JavaScript, rather than loading of additional HTML pages. A basic HTML layout is still required to run the quiz, as well as links to Bootstrap scripts. However, the simplicity of the HTML layout allows for easier porting of this quiz template to be a part of a more complex website structure. The CSS styling could then be changed, depending on the individual website design. Overall, this project demonstrates some of the practicality of DOM manipulation and utilizing local storage. Portability was kept in mind while designing the website. And last but not least, the project was a great exercise in coding.