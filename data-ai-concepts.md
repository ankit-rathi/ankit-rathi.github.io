---
layout: page
title: Data & AI Concepts
permalink: /data-ai-concepts/
---

## Data and AI Concepts
![](https://cdn-images-1.medium.com/max/2600/1*9LK8I2Up102oXcyFD-qbnw.png){:width="100%"}

<a name="table-of-contents"/>

### Table of Contents  
* [I Preface](#preface)  
* [II Data and AI Foundation](#data-and-ai-foundation)
* [III Data and AI Components](#data-and-ai-components)
* [IV Data and AI Platforms](#data-and-ai-platforms)
* [V Appendix](#appendix)

<a name="preface"/>

## [I Preface](https://ankitrathi.com/data-ai-concepts/preface/)


<a name="data-and-ai-foundation"/>

## II Data and AI Foundation
[Back to TOC](#table-of-contents)

*Topics Covered: Data and AI Introduction, Mathematics, IT/Programming, Business Domain*

In this section, I am going to build the foundation that is necessary to grasp before looking at components of data and AI platform. 

And we will start from scratch, first we will cover the basic concepts of data and AI and how these fields are connected, then we will focus on core concepts of mathematics, IT/programming and business domain etc.

### Data and AI Introduction

![](https://cdn-images-1.medium.com/max/810/1*xyslIRrIlWd3C-ReTAYTkw.png){:width="100%"}

### 1 Data Concepts 
*Topics Covered: Data, Data Vs Information, DIKW Pyramid, Different Aspects of Data (Formats, Scope, Biases), Structured, Semi-structured and Unstructured Data, Data Usage (Scientific Research, Business Management, Finance, Governance), Data Analysis*

![](https://cdn-images-1.medium.com/max/2600/1*rjy9ySLmVfw6bxfXc59w-A.png){:width="100%"}

#### 1.1 Data
Data is the back-bone of data-driven AI. So lets first understand what is data? 

Data is the raw fact without any context i.e. a number, symbol, character, word, codes, graphs, etc. 

![](https://cdn-images-1.medium.com/max/2600/1*IPkspG9qDOTW8AZK2Oq3aw.png){:width="100%"}

Data has originated as a plural form of Latin word 'Datum', which means 'a given fact'.

Broadly speaking, it can be any information in digital form, it can be output of sensing device or organ.

Loosely, data and information are used interchangeably, which is not correct, we will cover the difference in an upcoming section.

Data, information, knowledge and wisdom are closely related concepts, but each has its own role in relation to the other, and each term has its own meaning, we will also touch this part soon.

References: 
- https://harvard-iacs.github.io/2020-CS109A/lectures/lecture02/slides/Lecture02_Data.pdf
- https://docs.microsoft.com/en-us/learn/modules/explore-core-data-concepts/2-identify-need-data-solutions
- https://en.wikipedia.org/wiki/Data

#### 1.2 Datum, Data and Dataset

Mostly we talk about data but occassionally, you may hear terms like datum or dataset, lets understand the difference. Datum is single piece of information, which can be treated as an observation. Data is plural of datum, which we can say multiple observations. Dataset is a homogenous collection of data (each datum must have the same focus).

References: 
- https://harvard-iacs.github.io/2020-CS109A/lectures/lecture02/slides/Lecture02_Data.pdf

![](https://cdn-images-1.medium.com/max/2600/1*zr3gmtVjrfFHH46EDk0EpQ.png){:width="100%"}

#### 1.3 Information
When data is processed and put into context, it becomes information, which can be utilized by humans in significant way i.e. making decisions, forecasting etc

References: 
- https://en.wikipedia.org/wiki/Information

![](https://cdn-images-1.medium.com/max/2600/1*e7RLPPbGoQ_99dRC8kNJBw.png){:width="100%"}

![](https://cdn-images-1.medium.com/max/2600/1*Q2dcmqoaXCdtYGimmmphIQ.png){:width="100%"}

#### 1.4 Knowledge and Wisdom
When we put relevant information to work in a specific domain, it becomes knowledge. And when that knowledge is enhanced with first-hand experience, it becomes wisdom.

Lets relate it to an example:
- '100' number is data
- '100 miles' is information
- '100 miles is quite a far distance' is a knowledge
- '100 miles is very difficult to walk' is wisdom.

References: 
- https://en.wikipedia.org/wiki/DIKW_pyramid

#### 1.5 Different Aspects of Data

![](https://cdn-images-1.medium.com/max/2600/1*OSLT07CT7TTWXrYNmmYomA.png){:width="100%"}

##### Formats of Data
We can classify data formats in three categories as structured, semi-structured and unstructured:
- Structured data has a definite structure like table with rows and columns.
- Semi-structured data has some structure like JSON, key-value or graph database.
- Unstructured data has no specific structure like photos, audio and video files.

References: 
- https://docs.microsoft.com/en-us/learn/modules/explore-core-data-concepts/2-identify-need-data-solutions
- https://harvard-iacs.github.io/2020-CS109A/lectures/lecture02/slides/Lecture02_Data.pdf

![](https://cdn-images-1.medium.com/max/2600/1*AU28k8y-J8HsdV_ZFMiiaA.png){:width="100%"}

##### Scope of Data
Data can be classified in two categories based on scope:
- Population, which means we have access to all the data
- Sample, which means only a portion is available or feasible

We don't have access to all the data in mast of the cases, we can estimate the population from sample in those cases.

References: 
- https://harvard-iacs.github.io/2020-CS109A/lectures/lecture02/slides/Lecture02_Data.pdf

##### Biases in Data
Bias in data means over or under-representation of a sub-population, may not be intentional.
- Omission: using arguements from only one side
- Source selection: including more authoritative sources from one side 
- Story selection: sharing stories that agree with one side
- Placement: unimportant stories gets important placement in reputed media platforms
- Labelling: labeled on one side or missing labels on other side
- Spin: stories providing only one interpretation of an event

References: 
- https://harvard-iacs.github.io/2020-CS109A/lectures/lecture02/slides/Lecture02_Data.pdf

#### 1.6 Data Usage
Data is used in following fields:
- Scientific Research: Factual data is both, an essential resource and a valuable output
- Business Management: Data helps understand and improve processes
- Finance: Whoever has the best and the fastest information gains the edge
- Governance: Open data platform to help promote data-driven governance

References:
- https://en.wikipedia.org/wiki/Data

#### 1.7 Data Analysis
Data analysis is a process for obtaining raw data, and converting it into information useful for decision-making by users. Data, is collected and analyzed to answer questions, test hypotheses, or disprove theories.
- Data requirements
- Data collection
- Data processing
- Data cleaning
- Exploratory data analysis
- Data product
- Communication

References:
- https://en.wikipedia.org/wiki/Data_analysis

### 2 Technology Concepts
*Topics Covered: Technology, Information Technology, Data Structures and Algorithms, Data Processing and Storage, Data Models, Operational & Analytical Data, Databases, Data Warehouses, Streaming and Batch Data, ETL/ELT*

### 3 AI Concepts
*Topics Covered: Intelligence, Intelligent Agents, Applications (Web Search, Recommendation Systems, Self-driving Cars, Strategic Games), Aspects of AI (Search, Knowledge, Uncertainty, Optimization, Learning, Neural Networks, Language), Strong and Weak AI*

### 4 From Data To AI
*Topics Covered: Business Intelligence, Data Science, Machine Learning, Deep Learning, Artificial Intelligence*

### 5 Cloud Computing
*Topics Covered: Introduction, Public, Private and Hybrid Clouds, IaaS, PaaS and SaaS, Data and AI on Cloud, AWS, Azure and GCP*

### 6 Business Domain
*Topics Covered: Problem Solving, Problem Identification, Problem Definition, Prioritization, Root-Cause Analysis, Possible Solutions, Solution Evaluation, Cost-Benefit Analysis, Planning and Implementation*

<a name="data-and-ai-components"/>

## III Data and AI Components
[Back to TOC](#table-of-contents)

*Topics Covered: Data Governance, Data Architecture, Data Ingestion, Data Storage, Data Engineering, Data Science, Data Visualization, Data Operationalization*

### 7 Data Governance 
*Topics Covered: Data Governance Basics, Why Data Governance is Important?, Aspects of Data Governance, How to do Data Governance?*

### 8 Data Architecture
*Topics Covered: Data Architecture Basics, Why Data Architecture is Required?, How to build Data Architecture?*

### 9 Data Ingestion
*Topics Covered: Data Ingestion Basics, Types of Data Ingestion, Tools for Data Ingestion*

### 10 Data Storage
*Topics Covered: Data Storage Basics, Types of Data Storage, Tools for Data Storage*

### 11 Data Engineering
*Topics Covered: Data Engineering Basics, Tools for Data Engineering, Building Data Pipelines*

### 12 Data Science
*Topics Covered: Data Science Basics, Overall Process, Algorithms, Tools for Data Science*

### 13 Data Visualization
*Topics Covered: Data Visualization Basics, Why Data Visualization is Important?, Tools for Data Visualization*

### 14 Data Operationalization
*Topics Covered: Operationalization Basics, Why Operationalization is required?, Tools for Data AI Operationalization*

<a name="data-and-ai-platforms"/>

## IV Data and AI Platforms
[Back to TOC](#table-of-contents)

*Topics Covered: Open Source, AWS, Azure, GCP, Databricks, Snowflake*

### 15 Open Source
*Topics Covered: Building Data and AI Platform in Open Source*

### 16 AWS
*Topics Covered: Building Data and AI Platform in AWS*

### 17 Azure
*Topics Covered: Building Data and AI Platform in Azure*

### 18 GCP
*Topics Covered: Building Data and AI Platform in GCP*

### 19 Databricks
*Topics Covered: Building Data and AI Platform in Databricks*

### 20 Snowflake
*Topics Covered: Building Data and AI Platform in Snowflake*

<a name="appendix"/>

## V Appendix
[Back to TOC](#table-of-contents)

*Topics Covered: SQL, Python, UNIX and Shell Scripting, Data Structure and Algorithms*

### A Linear Algebra
*Topics Covered: Scalars, Vectors, Matrices and Tensors, Multiplying Matrices and Vectors, Identity and Inverse Matrices, Linear Dependence and Span, Norms, Special Kinds of Matrices and Vectors, Eigendecomposition, Singular Value Decomposition (SVD), The Moore Penrose Pseudoinverse, The Trace Operator, The Determinant, Principal Component Analysis*

### B Multivariate Calculus
*Topics Covered: Functions, Derivatives, Product Rule, Chain Rule, Integrals, Partial Derivatives, The Gradient, The Jacobian, The Hessian, Multivariate Chain Rule, Approximate Functions, Power Series, Linearization, Multivariate Taylor*

### C Probability
*Topics Covered: Probability, Conditional Probability, Random Variables, Probability Distributions*

### D Statistics
*Topics Covered: Statistics, Descriptive Statistics (Univariate, Bivariate, Multivariate Analysis, Function Models), Inferential Statistics (Sampling Distributions & Estimation, Hypothesis Testing, Correlation, Causation & Regression), Bayesian Statistics (Frequentist Vs Bayesian Statistics, Bayesian Inference, Test for Significance), Statistical Learning (Prediction & Inference, Parametric & Non-parametric methods, Prediction Accuracy and Model Interpretability, Bias-Variance Trade-Off)*

### E Operating System Basics
*Topics Covered: *

### F Data Structures and Algorithms Basics
*Topics Covered: Data Structures (Array, Linked List, Stack, Queue, Heap, Hashing, Binary Tree, Binary Search Tree, Graph, Matrix), Algorithms (Asymptotic Analysis, Searching and Sorting, Greedy Algorithms, Recursion, Dynamic Programming)*

### G Programming Basics
*Topics Covered: *

### H Database Systems Basics
*Topics Covered: *


### I SQL
*Topics Covered: SQL, Data Models, ER Diagrams, Tables, Temporary Tables, Selecting (SELECT, FROM, DISTINCT), Filtering (WHERE, AND, OR, IN, NOT, BETWEEN, NULLs, Wildcards), Ordering (ORDER BY, DESC), Aggregating (GROUP BY, HAVING, AVERAGE, COUNT, MAX, MIN), Subqueries, Joins (Cartesian, Inner, Outer <Left/Right>, Self), Sets (UNION, UNION ALL, INTERSECT), Aliases, Views, Subqueries (WITH AS)*

### J Python
*Topics Covered: Programming, Installation, Basic Syntax & Variable Types, Data Types and Conversion, Basic Operators and Loops, Functions, Exceptions and Modules, Data Science Specific Modules (NumPy, SciPy, Pandas, MatPlotLib, Scikit-Learn)*

### K UNIX and Shell Scripting
*Topics Covered: Operating System, Architecture, Basic UNIX Commands, Shell Scripting*


