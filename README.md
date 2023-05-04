Download Link: https://assignmentchef.com/product/solved-cs433-project-1
<br>
In this project, you will learn to use the concepts we have seen in the lectures and practiced in the labs on a real-world dataset, start to finish. You will do exploratory data analysis to understand your dataset and your features, do feature processing and engineering to clean your dataset and extract more meaningful information, implement and use machine learning methods on real data, analyze your model and generate predictions using those methods and report your findings.

Grading. Project 1 counts 10% to your final grade in the course. In Project 1, we will grade your code and report (each counting half) and you also obtain a competition score for feedback. (Project 2 will count 30%).

<h1>Logistics</h1>

Group formation. For Project 1, you will work in a team of 3 students, by your choice. If you are still searching for teammates, please use the discussion forum on Moodle. A good data science team combines a diverse set of skills, and greatly benefits from inter-disciplinary backgrounds.

Deliverables at a glance.            (More details and grading criteria further down)

<ul>

 <li>In Python. <em>No external libraries allowed! </em>For this first project, we want you to implement and use the methods we have seen in class. Only NumPy. Visualization libraries are always allowed, but only for visualization purposes. (External libraries will be allowed in Project 2).</li>

 <li>Written Report. You will write a maximum 2 page PDF report on your findings, using LaTeX.</li>

 <li>Competitive Part. To give you immediate feedback and a fair ranking, we use the competition platform aicrowd.com to score your predictions. You can submit whenever and almost as many times as you like, up until the final submission deadline.</li>

</ul>

The Dataset. For this course, we are providing you with our own online competition based on one of the most popular machine learning challenges recently – finding the Higgs boson – using original data from CERN.

<h1>Step 1 – Getting Started</h1>

Create an account using your epfl.ch email and head over to the competition arena

<a href="https://www.aicrowd.com/challenges/epfl-machine-learning-higgs-2019">https://www.aicrowd.com/challenges/epfl-machine-learning-higgs-2019</a>

Then, download the training dataset, available in .csv format. To load the data, use the same code we used during the labs. You can find an example of a .csv loading function in our provided template code from labs 1 and 2.

<h1>Step 2 – Implement ML Methods</h1>

We want you to implement and use the methods we have seen in class and in the labs. You will need to provide working implementations of the functions in Table 1. If you have not finished them during the labs, you should start by implementing the first ones to have a working toolbox before diving in the dataset.

<table width="624">

 <tbody>

  <tr>

   <td width="320">Function</td>

   <td width="304">Details</td>

  </tr>

  <tr>

   <td width="320">least squares GD(y, tx, initial w, max iters, gamma)</td>

   <td width="304">Linear regression using gradient descent</td>

  </tr>

  <tr>

   <td width="320">least squares SGD(y, tx, initial w, max iters, gamma)</td>

   <td width="304">Linear regression using stochastic gradient descent</td>

  </tr>

  <tr>

   <td width="320">least squares(y, tx)</td>

   <td width="304">Least squares regression using normal equations</td>

  </tr>

  <tr>

   <td width="320">ridge regression(y, tx, lambda )</td>

   <td width="304">Ridge regression using normal equations</td>

  </tr>

  <tr>

   <td width="320">logistic regression(y, tx, initial w, max iters, gamma)</td>

   <td width="304">Logistic regression using gradient descent or SGD</td>

  </tr>

  <tr>

   <td width="320">reg logistic regression(y, tx, lambda , initial w, max iters, gamma)</td>

   <td width="304">Regularized logistic regression using gradient descent or SGD</td>

  </tr>

 </tbody>

</table>

Table 1: List of functions to implement. In the above method signatures, for iterative methods, initial w is the initial weight vector, gamma is the step-size, and max iters is the number of steps to run. lambda  is always the regularization parameter. (Note that here we have used the trailing underscore because lambda is a reserved word in Python with a different meaning). For SGD, you must use the standard mini-batch-size 1 (sample just one datapoint).

You should take care of the following:

<ul>

 <li>Return type: Note that all functions should return: (w, loss), which is the last weight vector of the method, and the corresponding loss value (cost function). Note that while in previous labs you might have kept track of all encountered w for iterative methods, here we only want the last one.</li>

 <li>File names: Please provide all function implementations in a single python file, called implementations.py.</li>

 <li>All code should be easily readable and commented.</li>

 <li>Note that we might automatically call your provided methods and evaluate for correct implementation</li>

</ul>

Here are some good practices of scientific computing as a reference: <a href="https://arxiv.org/pdf/1609.00037">http://arxiv.org/pdf/1609.00037</a> or an older article <a href="https://arxiv.org/pdf/1210.0530">http://arxiv.org/pdf/1210.0530</a><a href="https://arxiv.org/pdf/1210.0530">.</a>

<h1>Step 3 – Submitting your Predictions</h1>

Once you have a working model (using the above methods or a modified one), you can send your predictions to the competition platform to see how your model is doing against the other teams. You can submit whenever and as many times as you like, until the deadline.

Your predictions must be in .csv format, see sample-submission.csv. You must use the same datapoint ids as in the test set test.csv. To generate .csv output from Python, use our provided helper functions in helpers.py (see project 1 folder on github).

After a submission, aicrowd.com will compute your score on the test set, and will show you your score and ranking in the leaderboard.

This is useful to see how you compare against other teams, but you should not consider this score as the only evaluation of your model. Always estimate your test error by using a local validation set, or local cross-validation! This is important to avoid overfitting the test set online. Also, it allows you to make experiments faster, and save uploading bandwidth :). You are only allowed a maximum of 5 submissions to the submission system per day.

Improving your predictions. While the above described method implementations must be part of your code submission, you can now implement additional modifications of these basic methods above. You can construct better features for the task, or perform better data preprocessing for this particular dataset, or even implement an additional modification of one of the above mentioned ML methods. Note that it is not allowed to use external libraries, code or data in this project. (It will be allowed in Project 2).

<h1>Step 4 – Final Submission of Your Project</h1>

Your final submission to the online system (a standard system as used for scientific conferences) must consist of the following:

<ul>

 <li>Report: Your 2 page report as .pdf</li>

 <li>Code: The complete executable and documented Python code, as one .zip file. Rules for the code part:

  <ul>

   <li><em>Reproducibility: </em>In your submission, you must provide a script run.py which produces <em>exactly </em>the same .csv predictions which you used in your best submission to the competition system.</li>

   <li><em>Documentation: </em>Your ML system must be clearly described in your PDF report and also welldocumented in the code itself. A clear ReadMe file must be provided. The documentation must also include all data preparation, feature generation as well as cross-validation steps that you have used.</li>

   <li>In addition to your customized system, don’t forget that your code submission must still also include the 6 <em>basic method implementations </em>as described above in step 2.</li>

   <li><em>No use of external ML libraries </em>is allowed in Project 1. (It will be allowed in Project 2).</li>

   <li>No external datasets allowed.</li>

  </ul></li>

</ul>

Submission URL: <a href="http://mlcourse.epfl.ch/">http://mlcourse.epfl.ch</a>

Submission deadline: Oct 28th, 2019 (midnight)

Step 5 – Profit

… &#x1f609;

<h1>Physics Background</h1>

The Higgs boson is an elementary particle in the Standard Model of physics which explains why other particles have mass. Its discovery at the Large Hadron Collider at CERN was announced in March 2013. In this project, you will apply machine learning techniques to actual CERN particle accelerator data to recreate the process of “discovering” the Higgs particle. For some background, physicists at CERN smash protons into one another at high speeds to generate even smaller particles as by-products of the collisions. Rarely, these collisions can produce a Higgs boson. Since the Higgs boson decays rapidly into other particles, scientists don’t observe it directly, but rather measure its“decay signature”, or the products that result from its decay process. Since many decay signatures look similar, it is our job to estimate the likelihood that a given event’s signature was the result of a Higgs boson (signal) or some other process/particle (background). In practice, this means that you will be given a vector of features representing the decay signature of a collision event, and asked to predict whether this event was signal (a Higgs boson) or background (something else). To do this, you will use the binary classification techniques we have discussed in the lectures.

If you’re interested in more background on this dataset, we point you to the longer description here: <a href="https://higgsml.lal.in2p3.fr/files/2014/04/documentation_v1.8.pdf">https://higgsml.lal.in2p3.fr/files/2014/04/documentation_v1.8.pdf</a><a href="https://higgsml.lal.in2p3.fr/files/2014/04/documentation_v1.8.pdf">.</a>

Note that understanding the physics background is not necessary to perform well in this machine learning challenge as part of the course.

<h1>Appendix</h1>

<h2>Grading Criteria</h2>

<ul>

 <li>Code (counts half). In Python. <em>No external libraries allowed! </em>For this first project, we want you to implement and use the methods we have seen in class. The code will be graded by two assistants independently, according to the criteria described above in Step 4.</li>

 <li>Written Report (counts half). You will write a maximum 2 page PDF report on your findings, using LaTeX. The code will be graded by two assistants independently, and we will provide you feedback. The main criteria will be if you were able to correctly implement the methods seen in class and explain your approach. This counts half for the written report. In addition, we will grade you on the scientific contribution you made additionally, to improve your predictions. For this part, the criteria are

  <ul>

   <li>scientific novelty</li>

   <li>creativity</li>

   <li>reproducibility</li>

   <li>solid comparison baselines supporting your claims</li>

   <li>writeup quality</li>

  </ul></li>

 <li>Competitive Part (counts only for fun). The final rank of your team in the (private) leaderboard is a strong indication how well you dealt with this practical ML problem. It allows you to experience the practical importance of each parts, the data cleaning, preprocessing, the ML model, and for example hyper-parameter optimization.</li>

</ul>

The competitive part will count in Project 2, but only for the standard tasks we provide. Here in this first toy project, as long as you’re not very far worse than all other teams, don’t spend too much time optimizing the rank yet. But make sure you can use the submission system and see the impact of your changes. Most important is that you understand the correct implementation of the algorithms and how their fair practical evaluation works, and thereby to prepare you for Project 2.

As usual, your code and report will be automatically checked for plagiarism.

<h2>Guidelines for Machine Learning Projects</h2>

Now that you have implemented few basic methods, you should use this toolbox on the dataset. Here are a few things that you might want to try.

Exploratory data analysis You should learn about your dataset – figure out which features are continuous, which ones are categorical, check if there are obvious relationships between the features, take a look at the distribution of each feature, and so on. Check <a href="https://en.wikipedia.org/wiki/Exploratory_data_analysis">https://en.wikipedia.org/wiki/Exploratory_data_analysis</a><a href="https://en.wikipedia.org/wiki/Exploratory_data_analysis">.</a>

Feature processing Cleaning your dataset by removing useless features and values, combining others, finding better representations of the features to feed your model, scaling the features, and so on. Check this article on feature engineering: <a href="http://machinelearningmastery.com/discover-feature-engineering-how-to-engineer-features-and-how-to-get-good-at-it/">http://machinelearningmastery.com/discover-feature-engineering-how-to</a><a href="http://machinelearningmastery.com/discover-feature-engineering-how-to-engineer-features-and-how-to-get-good-at-it/">engineer-features-and-how-to-get-good-at-it/</a><a href="http://machinelearningmastery.com/discover-feature-engineering-how-to-engineer-features-and-how-to-get-good-at-it/">.</a>

Determining whether a method overfits or underfits You should be able to diagnose the whether your model is over- or underfitting the data and take actions to fix the problems with your model. Recommended reading: <em>Advice on applying machine learning methods </em>by Andrew Ng: <a href="http://cs229.stanford.edu/materials/ML-advice.pdf">http://cs229.stanford.edu/materials/ML</a><a href="http://cs229.stanford.edu/materials/ML-advice.pdf">advice.pdf</a><a href="http://cs229.stanford.edu/materials/ML-advice.pdf">.</a>

Applying methods and visualizing Beyond simply applying the models we have seen, it helps to try to understand what the ML model is doing. Try to find out which datapoints are wrongly classified and, if possible, why this is the case. Then use this information to improve your model. Check Peter Domingo’s <em>Useful things to know about machine learning</em>: <a href="https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf">http://homes.cs.washington.edu/</a><a href="https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf">~</a><a href="https://homes.cs.washington.edu/~pedrod/papers/cacm12.pdf">pedrod/papers/cacm12.pdf</a>

Accurately estimate how well your method is doing By applying cross-validation and estimating the generalization error.

<h2>Report Guidelines</h2>

In addition to finding a good model for the data, you will need to explain your methodology in a report. For the first project, this will help you getting used to writing, and prepare you for the more extensive Project 2.

Clearly describe your used methods, state your conclusions and argue that the results you obtained make (or do not make) sense, and the reasons behind it. Keep the report short and to the point, with a strict limit of 2 pages (Project 2 will allow 4 pages). References are allowed to be put on a extra third page.

To get started more easily with writing the report, we provide you a LaTeX template here

<a href="https://github.com/epfml/ML_course/tree/master/projects/project1/latex-example-paper">github.com/epfml/ML</a> <a href="https://github.com/epfml/ML_course/tree/master/projects/project1/latex-example-paper">course/tree/master/projects/project1/latex-example-paper</a>

The file also contains some more helpful information on how to write a scientific report or paper. We will also help you learn it during the exercise session and office hours if you ask us.

For more guidelines on what makes a good report, see the grading criteria above. In particular, don’t forget to take care about

<ul>

 <li><em>Reproducibility: </em>Not only in the code, but also in the report, do include complete details about each algorithm you tried, e.g. what lambda values you used for ridge regression? How exactly did you do that feature transformation? how many folds did you use for cross-validation? etc…</li>

 <li><em>Baselines: </em>Give clear experimental evidence: When you added this new combined feature, or changed the regularization, by how much did that increase or decrease the test error? It is crucial to always report such obtained differences in the evaluation metrics, and to include several properly implemented baseline algorithms as a comparison to your approach.</li>

</ul>

Some additional resources on LaTeX:

<ul>

 <li><a href="https://github.com/VoLuong/Begin-Latex-in-minutes">https://github.com/VoLuong/Begin-Latex-in-minutes</a> – getting started with LaTeX</li>

 <li><a href="http://www.maths.tcd.ie/~dwilkins/LaTeXPrimer/">http://www.maths.tcd.ie/</a><a href="http://www.maths.tcd.ie/~dwilkins/LaTeXPrimer/">~</a><a href="http://www.maths.tcd.ie/~dwilkins/LaTeXPrimer/">dwilkins/LaTeXPrimer/</a> – tutorial on LaTeX</li>

 <li><a href="http://www.stdout.org/~winston/latex/latexsheet-a4.pdf">http://www.stdout.org/</a><a href="http://www.stdout.org/~winston/latex/latexsheet-a4.pdf">~</a><a href="http://www.stdout.org/~winston/latex/latexsheet-a4.pdf">winston/latex/latexsheet-a4.pdf</a> – cheat sheet collecting most of all useful commands in LaTeX</li>

 <li><a href="http://mirror.switch.ch/ftp/mirror/tex/info/first-latex-doc/first-latex-doc.pdf">http://mirror.switch.ch/ftp/mirror/tex/info/first-latex-doc/first-latex-doc.pdf</a> – example how to create a document with Latex</li>

 <li><a href="https://en.wikibooks.org/wiki/LaTeX">http://en.wikibooks.org/wiki/LaTeX</a> – detailed tutorial on LaTeX</li>

</ul>

<h3>Producing figures for LaTeX in Python</h3>

There are some good visualization tools in Python. “matplotlib” is probably the single most used Python package for 2D-graphics. The relevant tutorials are as follow:

<ul>

 <li>Matplotlib tutorial: <a href="http://www.labri.fr/perso/nrougier/teaching/matplotlib/">http://www.labri.fr/perso/nrougier/teaching/matplotlib/</a></li>

 <li>Matplotlib tutorial: <a href="https://sites.google.com/site/scigraphs/tutorial">https://sites.google.com/site/scigraphs/tutorial</a></li>

 <li>Matplotlib Tutorial: <a href="https://jakevdp.github.io/mpl_tutorial/">http://jakevdp.github.io/mpl_tutorial/</a></li>

</ul>

Regarding other useful Python data visualization libraries, please refer to this <a href="https://jakevdp.github.io/mpl_tutorial/">blog</a> for more information.