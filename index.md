---
title: Schedule
layout: page
icon: "far fa-calendar-alt"
---

Required readings and lecture videos are listed below for each module.
Readings from [\[ISLR\]](https://www.statlearning.com) are always required while those from [\[ESL\]](https://web.stanford.edu/~hastie/ElemStatLearn/) are optional and supplemental. 


<div class="text-center">
<div class="btn-group" role="group">
  <a role="button" class="btn btn-secondary text-white" href="#0-introduction-and-review">0 Intro</a>
  <a role="button" class="btn btn-secondary text-white" href="#1-model-accuracy">1 Model Checks</a>
  <a role="button" class="btn btn-secondary text-white" href="#2-regularization-smoothing-and-trees">2 Regression</a>
  <a role="button" class="btn btn-secondary text-white" href="#3-classification">3 Classification</a>
  <a role="button" class="btn btn-secondary text-white" href="#4-modern-techniques">4 Modern</a>
  <a role="button" class="btn btn-secondary text-white" href="#5-unsupervised-learning">5 Unsupervised</a>
  <a role="button" class="btn btn-secondary text-white" href="#f-final-exam">F Final</a>
</div>
</div>

<br>

<div class="alert alert-primary" role="alert">
All lecture slides as <code>.Rmd</code> files are available <a href="https://github.com/UBC-STAT/stat-406-lectures">here</a>.
</div>

<div class="alert alert-primary" role="alert">
Handouts for some lectures (coding files, pdfs) are available <a href="https://github.com/UBC-STAT/stat-406-lectures/handouts">here</a>.
</div>

If you want `.pdf`s of the lecture slides (requires Google Chrome to be installed)

1. Clone the repo from <https://github.com/UBC-STAT/stat-406-lectures>.
1. Open the project in RStudio.
1. Run `install.packages("renderthis")`
1. To convert a set to pdf, run, say,  `renderthis::to_pdf("slides/04-bias-variance.html")`.
1. Repeat for any slides you want.
1. If you want to do it for all slides at once (not advised since I update them a few times before class) you can do 
    
    ```r 
    purrr::walk(
      list.files("slides", ".html", full.names = TRUE), 
      ~ renderthis::to_pdf(.x)
    )
    ```

## 0 Introduction and Review

Required reading below is meant to reengage brain cells which have no doubt forgotten all
the material that was covered in STAT 306 or CPSC 340. We don't presume that you remember all these details, but that, upon rereading, they at least sound familiar. If this all strikes you as completely foreign, this class may not be for you.

Required reading  
: \[ISLR\] 2.1, 2.2, and Chapter 3 (this material is review)

Optional reading
: \[ESL\] 2.4 and 2.6

Handouts
: Programming in `R` [`.Rmd`](handouts/00-programming.Rmd), [`.pdf`](handouts/00-programming.pdf)
: Using in RMarkdown [`.Rmd`](handouts/00-rmarkdown.Rmd), [`.pdf`](handouts/00-rmarkdown.pdf)


| Date      | Slides                                                                                 | Deadlines |
|:----------|:---------------------------------------------------------------------------------------|:----------|
| 6 Sep 21  | (no class, Imagine UBC)                                                                |           |
| 8 Sep 21  | [Intro to class](slides/00-intro-to-class.html), [Git](slides/00-version-control.html) |           |
| 13 Sep 21 | [Understanding R / Rmd](slides/00-r-review.html)                                  |           |
| 15 Sep 21 | [LM review](slides/01-lm-review.html), [LM Example](slides/02-lm-example.html)         |           |
{: .table .table-striped}




## 1 Model Accuracy

Topics  
: Model selection; cross validation; information criteria; stepwise regression

Required reading  
: \[ISLR\] Ch 2.2 (not 2.2.3), 5.1 (not 5.1.5), 6.1, 6.4

Optional reading
: \[ESL\] 7.1-7.5, 7.10

| Date      | Slides                                                                                                       | Deadlines         |
|:----------|:-------------------------------------------------------------------------------------------------------------|:------------------|
| 20 Sep 21 | [Regression function](slides/03-regression-function.html), [Bias and Variance](slides/04-bias-variance.html) |                   |
| 22 Sep 21 | [Risk estimation](slides/05-estimating-test-mse.html), [Info Criteria](slides/06-information-criteria.html)  |                   |
| 27 Sep 21 | [Greedy selection](slides/07-greedy-selection.html)                                                          |                   |
| 29 Sep 21 |                                                                                                              | HW 1 due |
{: .table .table-striped}




## 2 Regularization, smoothing, and trees

Topics  
: Ridge regression, lasso, and related; linear smoothers (splines, kernels); kNN

Required reading  
: \[ISLR\] Ch 6.2, 7.1-7.7.1, 8.1, 8.1.1, 8.1.3, 8.1.4

Optional reading
: \[ESL\] 3.4, 3.8, 5.4, 6.3

| Date      | Slides                                                                           | Deadlines |
|:----------|:---------------------------------------------------------------------------------|:----------|
| 4 Oct 21  | [Ridge](slides/08-ridge-regression.html), [Lasso](slides/09-l1-penalties.html)   |           |
| 6 Oct 21  | [NP 1](slides/10-basis-expansions.html), [NP 2](slides/11-kernel-smoothers.html) |           |
| 11 Oct 21 | [Why smoothing?](slides/12-why-smooth.html)                                      |           |
| 13 Oct 21 | [CV for comparison](slides/00-cv-for-many-models.html), [Other](slides/13-gams-trees.html) |           |
| 18 Oct 21 |                                                                                  | HW 2 due  |
{: .table .table-striped}



## 3 Classification

Topics  
: logistic regression; LDA/QDA; naive bayes; trees

Required reading  
: \[ISLR\] Ch 2.2.3, 5.1.5, 4-4.5, 8.1.2

Optional reading
: \[ESL\] 4-4.4, 9.2, 13.3

| Date      | Slides                                                                                                         | Deadlines |
|:----------|:---------------------------------------------------------------------------------------------------------------|:----------|
| 20 Oct 21 | [Classification](slides/14-classification-intro.html), [LDA and QDA](slides/15-LDA-and-QDA.html)               |           |
| 25 Oct 21 | No class  |           |
| 27 Oct 21 | [Logistic regression](slides/16-logistic-regression.html), [Gradient descent](slides/00-gradient-descent.html)        |           |
| 1 Nov 21  | [Other losses](slides/00-classification-losses.html), [Nonlinear](slides/17-nonlinear-classifiers.html)                                                                   |       |
{: .table .table-striped}



## 4 Modern techniques

Topics  
: bagging; boosting; random forests; neural networks

Required reading  
: \[ISLR\] 5.2, 8.2, 10.1, 10.2, 10.6, 10.7 

Optional reading
: \[ESL\] 10.1-10.10 (skip 10.7), 11.1, 11.3, 11.4, 11.7

| Date      | Slides                                                                                                        | Deadlines |
|:----------|:--------------------------------------------------------------------------------------------------------------|:----------|
| 3 Nov 21  | [The bootstrap](slides/18-the-bootstrap.html)                                                                 | HW 3 due     |
| 8 Nov 21  | [Bagging and random forests](slides/19-bagging-and-rf.html), [Boosting](slides/20-boosting.html)              |     |
| 10 Nov 21 | (no class, Midterm Break)                                                                                     |           |
| 15 Nov 21 | [Intro to neural nets](slides/21-nnets-intro.html), [Estimating neural nets](slides/22-nnets-estimation.html) |           |
| 17 Nov 21 | [Neural nets wrapup](slides/23-nnets-other.html)                                                              |           |
| 22 Nov 21 |                                                                                                               | HW 4 due  |
{: .table .table-striped}



## 5 Unsupervised learning

Topics  
: dimension reduction and clustering

Required reading  
: \[ISLR\] 12

Optional reading
: \[ESL\] 8.5, 13.2, 14.3, 14.5.1, 14.8, 14.9


| Date      | Slides                                                                                        | Deadlines          |
|:----------|:----------------------------------------------------------------------------------------------|:-------------------|
| 24 Nov 20 | [Intro to PCA](slides/24-pca-intro.html), [Issues with PCA](slides/25-pca-issues.html)        |                    |
| 29 Nov 20 | [PCA v KPCA](slides/26-pca-v-kpca.html)                                                       |                    |
| 1 Dec 20  | [K means clustering](slides/27-kmeans.html), [Hierarchical clustering](slides/28-hclust.html) |                    |
| 6 Dec 20  |                                                                                               | HW 5 due |
{: .table .table-striped}




## F Final exam

Sunday, December 18 from 19:00&ndash;21:15 [LIFE 2201](https://learningspaces.ubc.ca/classrooms/life-2201)  
(formally known as the Student Union Building)

<div class="alert alert-danger" role="alert">Do not leave Vancouver before the final exam date.</div>



* In person attendance is required (per Faculty of Science guidelines)
* You must bring your computer as the exam will be given through Canvas
* Please [arrange to borrow](https://services.library.ubc.ca/computers-technology/technology-borrowing/) one from the library if you do not have your own. Let me know ASAP if this may pose a problem.
* You may bring 2 sheets of front/back 8.5x11 paper with any notes you want to use. No other materials will be allowed.
* There will be no required coding, but I may show code or output and ask questions about it.
* It will be entirely multiple choice / True-False / matching, etc. Delivered on Canvas.

### Schedule of Office Hours before the Final

* December 6 in ESB 4182 (or 4192 if necessary, this is my usual one)
* December 8, 2-3:30 in ESB 3174 (TA)
* December 12, 4-5:30 on Zoom (use the link on Canvas, TA)
* December 13, 2-3 in ESB 4192 (Daniel)
* December 15, 11-12 in ESB 4192 (Daniel)
* December 16, 10:30-12 on Zoom (use the link on Canvas, TA)

<!--

### Procedures (shown in Canvas Announcement)

I know many of you are concerned about rapidly escalating case numbers, and I share your concerns. According to Dr. Henry's press briefing today, there has (until now) been very little spread in lecture halls, in stark contrast to what happens in parties or social gatherings. Here is the current plan (subject to change if the University makes changes). The room is very large (holds 260 people), so there should be plenty of space to spread out.


1. The Exam remains in-person as scheduled. This is UBC policy until it changes. I was told explicitly that ONLY the Dean can decide to move it online. See also the most recent message from Pres. OnoLinks to an external site.. 
1. If you are feeling ill, please contact your Faculty Advising office for an SD. I was told that this will likely be granted. Please do not come to the exam.
1. Please wear a high quality mask if you can (rather than a non-medical mask). Please keep it on at all times (fitting tightly over your nose and mouth) and refrain from drinking. No eating is allowed.
1. Please arrive early. We will let you in as you arrive to try to minimize close-quarters gathering.
1. The Canvas Exam will not open until 8:45. This should allow us a bit of extra time to seat you and go over instructions.
1. We will check your UBC ID as you arrive. You will not be allowed to take the exam without it. See UBC Policy hereLinks to an external site..
1. You may bring 2 sheets of paper, with handwritten notes. Front and back. We will glance at these at the same time we check your ID. We will not collect them.
1. We will NOT use Lockdown browser, but any student caught looking at any window or program other than Canvas will be warned, and their mark may be lowered, potentially to 0. 
1. I would like students to remain seated until 10am. At 10, we will allow any students who are done to leave all at once. After that, we will ask students to remain until the Exam ends at 10:45. This is to minimize possibly contagious students from climbing over others. We will conduct both these exoduses in an organized fashion, row by row.
1. For the same reason, we will limit bathroom breaks to emergencies only. If truly necessary, we can let you go at 10am with the first exodus. Please plan accordingly.
1. We will not be mingling to answer clarifying questions. We will handle any "inaccurate questions" afterward as needed. This is for everyone's safety.
1. All told, you will have 1 hour 55 minutes for the exam (begin at 8:45, end at 10:45, 5 minute break at 10 for early departures).
1. There have been reports of students pulling fire alarms during exams in the last week. If this or something else disrupts the exam, there are official policies that apply. They sound "not fun", so hopefully this can be avoided.

### Office Hours

See Canvas/Zoom for links.

-->
