Instructions for 432 Project 1
================

  - [Introduction](#introduction)
      - [Project 1 involves two tasks.](#project-1-involves-two-tasks.)
      - [Am I working alone, or in a
        group?](#am-i-working-alone-or-in-a-group)
      - [What Makes an Acceptable Data
        Set?](#what-makes-an-acceptable-data-set)
  - [Deliverable 1. The Proposal](#deliverable-1.-the-proposal)
      - [The Nine Parts of Your
        Proposal](#the-nine-parts-of-your-proposal)
          - [Evaluating the Project 1
            Proposal](#evaluating-the-project-1-proposal)
      - [The Group Meetings](#the-group-meetings)
  - [Deliverable 2. The Poster](#deliverable-2.-the-poster)

As a substantial part of your course grade, you will complete two
Projects this semester. This document describes Project 1. Instructions
for Project 2 will appear later in the term.

# Introduction

It is hard to learn statistics (or anything else) passively; concurrent
theory and application are essential. Expert clinical researchers and
statisticians repeatedly emphasize how important it is that people be
able to write well, present clearly, work to solve problems, and show
initiative. This project assignment is designed to help you develop your
abilities and have a memorable experience.

In Project 1, you will be analyzing, presenting and discussing a pair of
regression models, specifically a linear regression and a logistic
regression, describing a data set you identify.

## Project 1 involves two tasks.

1.  Develop a proposal, which includes a presentation of the data. This
    proposal is due in mid-February. The proposal is graded by the TAs
    using a formal rubric prepared by Dr. Love. You will iterate (as
    necessary) on your proposal until you receive full credit. The
    proposal is worth 50% of the project 1 grade. This document
    describes the proposal in detail.

2.  Develop an electronic poster of your work. This poster is due in
    early March. The poster is evaluated by Dr. Love. The poster is
    worth the remaining 50% of the project 1 grade. Details on the
    poster will be provided by 2020-01-28.

See the [Course
Calendar](https://github.com/THOMASELOVE/2020-432/blob/master/calendar.md)
for deadlines.

## Am I working alone, or in a group?

You can choose either to work alone, or with one other person, to
complete Project 1.

  - At times, we may require you to share drafts of your work with other
    people in small groups, but the actual data collection, analysis and
    report-building work is for you (or you and your partner) to do.

## What Makes an Acceptable Data Set?

1.  **Shareable with the World**. The data must be available to you, and
    shared with me and everyone else in the world (without any
    identifying information) as a well-tidied .csv file on 2020-02-14.
    If the data is from another source, the source (web or other) must
    be completely identified to me. Ongoing projects that require
    anyone’s approval to share data are not appropriate for Project 1,
    but can be used (with Dr. Love’s approval) for Project 2.
    
      - You should have the data in R by 2020-02-05, so that you will
        have sufficient time to complete the other elements of this
        proposal. Any data you cannot have by that time is a bad choice.
      - For Project 1, you may not use any data set that was used in the
        431 or 432 teaching materials. You may not use any data set
        included in [an R package that we are
        installing](https://github.com/THOMASELOVE/2020-432/blob/master/software.md)
        this semester, other than NHANES.
      - You must use meaningfully different data sets in 432 Projects 1
        and 2.
      - You **are** allowed to use NHANES data in Project 1, but only if
        you are combining information from at least three NHANES data
        sets. If you used NHANES data in your 431 project, you can use
        NHANES data again this semester, but you must study new
        outcomes.
      - You are permitted to use BRFSS data, but you are not permitted
        to use data from SMART BRFSS, since we will be using that
        regularly in class.

2.  **Size**. A **minimum** of 100 complete observations are required on
    each variable. It is fine if there are some missing values, as well,
    so long as there are at least 100 rows with complete observations on
    all variables you intend to use in each model. The **maximum** data
    set size is 1000 observations, so if you have something larger than
    that, you’ll need to select a subset.

3.  **Outcomes**. The columns must include at least one quantitative
    outcome and one binary categorical outcome. If necessary, the binary
    outcome can be generated from the quantitative outcome (as an
    example, your quantitative outcome could be resting heart rate in
    beats per minute, and your binary outcome could be whether the
    resting heart rate is below 70 beats per minute.)

4.  **Inputs**. You will need at least four regression inputs
    (predictors) for each of your two models. At least one of the four
    must be quantitative (a variable is **not** quantitative for this
    purpose unless it has at least 10 different, ordered, observed
    values), *and* at least one must be multi-categorical (with at least
    3 categories, each containing a minimum of 30 subjects) for each
    model. Your other inputs can represent binary, multi-categorical or
    quantitative data. You can examine different candidate predictors
    for each outcome, or use the same ones in both your linear and
    logistic regression models. Depending on your sample size, you can
    study more regression inputs. Specifically, if you have N complete
    observations in your data set, you are permitted to study up to 4 +
    (N-100)/100 candidate regression inputs, rounding down.

# Deliverable 1. The Proposal

The proposal is to be submitted via file uploads to
[Canvas](https://canvas.case.edu).

Your proposal will include - (a) a single `.csv` file of the data you
have chosen - (b) a R Markdown file containing the information listed
below, and - (c) an HTML document which is the unedited result of
knitting your Markdown file.

## The Nine Parts of Your Proposal

The nine pieces of information we should find in the Markdown and HTML
versions of your proposal are:

1.  Complete information on the source of the data: how did you get it,
    how was it gathered, by whom, in what setting, for what purpose, and
    using what sampling strategy.
2.  Code to load the raw `.csv` file into a tibble, and tidy/clean up
    the data to be useful for your modeling work.
3.  A listing of the tibble, with all variables correctly imported (via
    your code) as the types of variables (factor/integer/numeric, etc.)
    that you need for modeling. Be sure that your listing specifies the
    number of rows and number of columns in your tidy data set.
4.  A description (one or two sentences) of who or what the subjects
    (rows) are in your data set.
5.  A code book, which provides, for each variable in your tibble, the
    following information:
      - The name of the variable used in your tibble
      - The type of variable (binary, multi-categorical, quantitative)
      - The details for each variable
          - if a categorical variable, what are the levels, and what %
            of subjects fall in each category
          - if a quantitative variable, what is the range of the data,
            and what are the units of measurement
          - if there are missing data, tell us how many observations are
            missing, and why, if you know why.
6.  A sentence or two for each variable (column) providing a description
    of what the variable measures or describes, in English.
7.  A sentence or two telling us what you will use your linear
    regression model to explain or predict, *followed by* a sentence or
    several telling us very precisely which (quantitative) variable will
    serve as your outcome in your linear regression model, and which
    four (or more) candidate predictors you intend to use for that
    model.
8.  A sentence or two telling us what you will use your logistic
    regression model to explain or predict, *followed by* a sentence or
    several telling us very precisely which (binary) variable will serve
    as your outcome in your logistic regression model, and which four
    (or more) candidate predictors you intend to use for that model.
9.  An affirmation that the data set meets all of the requirements
    specified here, most especially that the data can be shared freely
    over the internet, and that there is no protected information of any
    kind involved. You need to be able to write “I am certain that it is
    completely appropriate for these data to be shared with anyone,
    without any conditions. There are no concerns about privacy or
    security.” If you are unsure whether this is true, select a
    different data set.

### Evaluating the Project 1 Proposal

  - Your project will be evaluated on a scale of 0-10, with one point
    for submitting all necessary materials (.csv, .Rmd and HTML)
    successfully, and then one additional point for each of the nine
    tasks if they are successfully completed.
  - If you receive a grade lower than 10, you will need to redo until
    you reach 10. Redos are expected within 48 hours of receipt of the
    redo request.

The full [Project 1 Proposal
Rubric](https://github.com/THOMASELOVE/2020-432/blob/master/projects/project1/project1_proposal_rubric.md)
is available now. Please review that material closely, so that your
submission will meet all requirements and score a 10 on the first try.

## The Group Meetings

  - On 2020-02-27, you will meet during class time to present your
    proposal work, and any subsequent work you have completed on your
    portfolio. This important session will give you the opportunity to
    present a piece of your work to some of your colleagues, and get
    meaningful feedback from them on the decisions you have made. The
    TAs will run this session, as Dr. Love will be out of town.

# Deliverable 2. The Poster

You’ll be using the [posterdown
package](https://github.com/brentthorne/posterdown) to build your poster
for Project 1.

  - Learn more about `posterdown` [at its
    repository](https://github.com/brentthorne/posterdown), and with
    this [installation and usage
    guide](https://github.com/brentthorne/posterdown/wiki/Installation-&-Usage-Guide).

Further details on the poster should be available by 2020-02-01.
