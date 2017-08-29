# LECTURE 1: CLASS POLICIES, TOOLS AND TECHNOLOGIES

| Week of 8/30  | [Lecture Notes](https://github.com/kmsaumcis/mcis6273_f17_datamining/tree/master/lecture_notes/)|
|-------------:|:-------------------------------------------------------------------|
| **Content**  |  class policies, class tools, introduction, what this course is about, data mining: tools, technologies and techniques |
| **Expected<br/>Outcomes** | &#8226; overview of course policies<br/>&#8226; overview of data mining concepts, algorithms, methodologies<br/>&#8226; installation of Anaconda and Python 3.6<br/>&#8226; introduction to Jupyter Notebooks<br/>&#8226; creation of Github account<br/> |
| **Readings &<br/>Supplemental** | **REQUIRED**<br/>&raquo; 2014\. Zaki, Mohammed J and Meira Jr, Wagner; [*Data mining and analysis: fundamental concepts and algorithms*](http://www.dataminingbook.info/pmwiki.php)\. &#8594; **ch.1**<br/>&raquo; 2014\. Leskovec, Jure and Rajaraman, Anand and Ullman, Jeffrey David; [*Mining of massive datasets*](http://www.mmds.org/)\. &#8594; **ch.1**<br/>&raquo; 2011\. Han, Jiawei and Pei, Jian and Kamber, Micheline; [*Data mining: concepts and techniques*](https://ia800300.us.archive.org/5/items/DataMiningConceptAndTechniques2ndEdition/Data.Mining.Concepts.and.Techniques.2nd.Ed-1558609016.pdf)\. &#8594; **ch.1, ch.2**<br/><br/>**OPTIONAL**<br/>&rsaquo; 2012\. Downey, Allen; [*Think Python*](http://www.greenteapress.com/thinkpython/thinkpython.html)\. &#8594; **ch.1-ch.3**<br/>&rsaquo; \(website\) \-\- 2017; *The Periodic Table of Data Science*: [https://www\.datacamp\.com/community/blog/data\-science\-periodic\-table\#gs\.TF297Gsm](https://www.datacamp.com/community/blog/data-science-periodic-table#gs.TF297Gsm)\. &#8594; **Familiarize yourself with the entire table.**<br/> |
| **Homework** | **DUE:** Monday, 9/4 - midnight<br/>Please see the  Blackboard/[Github repo](https://github.com/kmsaumcis/mcis6273_f17_datamining) for what to turn in. |

---

# NOTES

Welcome to the course!  Over the coming weeks we're going to have a lot of fun, learn a lot about data mining tools, technique and algorithms and end up prepared and excited to do analyses and explorations of our own!

# INTRODUCTION TO DATA MINING

At the core of data mining is the exploration of _finding meaningful patterns in data_, often in pursuit of patterns that will help explain a phenomenon that would ordinarily not be possible with human effort alone.  Data mining borrows much of its heritage from applied mathematics and statistical thinking, but with the rise of _massive data_, traditional statistical techniques often fall short and require completely different algorithmic approaches and computational technologies.

This _massive data_ cannot be overstated. When we look at even a small susbset of the "dataverse" (a term I am loosely using to encompass the whole of data), data from the web and social media, [some estimates suggest](http://wersm.com/how-much-data-is-generated-every-minute-on-social-media/#prettyPhoto) that data is being created at a rate never before seen.  For example every minute:
* over 300 hours of YouTube video is being uploaded, 
* 77,000+ hours of video are being streamed over Netflix,
* 51,000+ apps are downloaded from the Apple iTunes store,

and so on.  Our ability to consume this data, let alone make sense of it is indeed being challenged, hence the rapid rise of data mining, machine learning and data science technologies in the last decade.

Data mining is a discipline unto itself, but it can easily be considered a subset of the broader area of _data science_ which encompasses machine learning, data analytics, data visualization, data engineering, etc.  Data mining, is a common thread throughout all of data science, and as such the topics we cover will represent a broad swath of nearly all of what is now termed "data science".

One common summarization of "data science" has been given by [Drew Conway](http://drewconway.com/zia/2013/3/26/the-data-science-venn-diagram) that suggests data science is the intersection of _software engineering_, _mathematical modeling and statistical analysis_ applied over a particular _domain_ or set of complementary domains, with **data** being at the foundation of it all.

<img src="assets/Data_Science_VD.png"/>


Our attention will largely be on the _statistical and mathematical_, _software engineering_ components, and we will add to this _data engineering_, _data visualization_, with an eye towards specific areas of _text mining_, _social network analysis_ and _data ethics_.

While some argue the term "data mining" might be subsumed by "data science" or that is a bit of a misnomer, we'll stick with the term, knowing that while we may "mine" for data, the outcomes of such mining should be carefully considered in the context of whether such outcomes are meaningful or not.  We will come to understand that many results and outcomes of data analyses must be couched carefully as to avoid misinterpretation, since often there may be outcomes that confirm what we _want_ rather than what _actually exists_, or even worse something that _doesn't_ exist but rather produces enough signal to seem meaningful, but in reality is just noise.  This is no different than the criticisms lodged at statistical models that confirm the relationships being sought, rather than the actual relationships that truly describe a phenomenon.

## DATA MINING WORKFLOW
The data mining process can be summarized as follows:

**DATA ENGINEERING AND PREPARATION**
> Data cleaning<br/>
Data integration<br/>
Data selection<br/>
Data transformation
    
**DATA  EXPLORATION, MODEL BUILDING AND ANALYSIS**
> Statistical analysis<br/>
Pattern mining<br/>
Prediction<br/>
Classification<br/>
Clustering

**EVALUATION AND MODEL INTERPRETATION**
> Pattern evaluation<br/>
Model interpretation and evaluation<br/>

**PRESENTATION**
> Visualization and Reporting<br/>
Data narratives<br/>

You might look at the process and think that most of your time will be spent in analysis, but this is often not the case.  As [we'll explore soon]() data engineering and preparation can _often be the most time consuming component_ of the process, since  the type of data (structured, unstructured), the source of the data (database, online, etc.) and the volume of data might require significant cleaning, selection and transformation.  Luckily, there are many tools that can ease the complexity of these tasks. 

## DATA SOURCES

Data mining can be carried out over a number of different data sources, the most common of which are :

* relational databases
* data warehouses
* transactional databases
* object, temporal, time-series and sequence databases
* real-time data streams

Within an enterprise, there are many sources of data that may be the target of a data mining exploration.  For example, some businesses keep extensive relational databases on products, draw from transactional databases for retail sales data or tap large data warehouses to get segments of data required to answer more nuanced questions of importance to a business need.

Take for example a company that stores customer profiles but may want to fully understand how their customer demographics play into the sales of specific products.  They might be interested in knowing if certain products are associated with certain income brackets, etc.  Such analysis may be easy to perform if customer income is known (or can be drawn on from a data warehouse), otherwise such an analysis may require data from another source external to the company.

_Internal data sources_, are an important source of data and will often be a _primary_ source of data when embarking on an analysis, but _external data sources_ are often equally important for data mining tasks.  For example, the [US Census Bureau](http://census.gov) keeps extensive data on the demographics of the US and economy.  A company may want to correlate data from the Census, for example, with their own data or supplement data they have with data from a government source, since such sources tend to be statistically reliable and consistent.  These data may be accessed directly or stored locally and updated when necessary.

External sources are plentiful, and many are *open* (e.g. most if not all public government data), yet some external data may come at a cost, for example, sports data or data from companies that collect data of a particular kind (social media, web analytics, etc.).  For this course, we will work with open data sources, keeping in mind that some data may not be so freely available.

## DATA MINING FUNCTIONALITIES

We will focus our attention on at least five major data mining functionalities listed in the table below.  Each entry in the table includes information about the typical scenarios these functionalities appear in.

| Functionality  |  Scenario |
|:---------------:|:--------------------------------------------|
|**_Class summarization and description_** | Determining the characteristic of a class or group in a data set.  For example, summarizing the various types of users to a website; or the kinds of workouts common in a gym. |
|**_Frequent patterns, association and correlations_** | Determining the patterns that are commonly associated with one another.  For example, discovering that people who shop at a certain time of day are likely to buy coffee when they also buy cookies; or that certain combinations of car options are associated with certain types of car colors.  |
|**_Clustering_**| Uncovering patterns in data that are typically not know or previously categorized.  For example, determining the topics within a set of unknown tweets; or finding the usage patterns of a particular application.  |
|**_Classification and Prediction_** | Assigning classes or making predictions given some prior knowledge about those classes.  For example, given a series of images of cats, being able to correctly recognize a previously unseen picture of a cat; or making a prediction about the outcome of a baseball game, given each teams' prior performance, records and personnel. |
|**_Outlier analysis_** | Discerning data that may appear to be outside the typical characteristics of a dataset, when such data is not noise and instead rises to the level of a rare, but nonetheless interesting data point.  For example, detecting network traffic that represents potential security threats to a server.| 

#  TOOLS

There are three primary tools we will used in this course:

* [Github](https://github.com): we will use this for our course materials, in conjunction with Blackboard.
* [Python](https://python.org): Python is one of a few languages widely used in data mining, machine learning and data science.  It has easy syntax and powerful expressiveness, and is backed by a strong ecosystem of tools and libraries for the entire data mining workflow.
* [Jupyter Notebooks](https://jupyter.org): Jupyter Notebooks (also knows and "ipynb"'s"or "nb"'s) are an important tool in analysis, visualization and narrative building (reporting).  They are quickly beecoming the _de facto_ tool for building and distributing data analysis code.

## Github 



[Github](https://www.github.com) is a system / web application / platform that provides a beautiful way to store, view, manage, share and revise code.  While the primary content on Github is _running_ software, whether that be in C, Java, HTML, Python or the many hundreds of other languages in popular use today, it can also be a place for traditional text files (data, papers) and other binary data (Word/Excel documents, images, etc.)  Github's strength is in the ability for it to facilitate software collaboration, and today it is the premier place on the web for large scale open-source, collaborative software projects.  Though open and public projects are Github's forte, it provides the ability for you to host private projects and allows you to make the decision later whether it is appropriate to make such projects public or not.

Github is built on top of what is called **git**, which is a __revision control system__.  The core concept behind such systems is that they manage your text-based code files and allow you to keep track of the changes (revisions) to those files.  In a system like [**git**](https://git-scm.com/) you can invite others to work on your code as well, which can allow more than one person to make contributions to the code.  What is even more useful is that such changes can be tracked across a project so that those contributions and changes can be seen, reviewed, modified and otherwise managed.  Thus, when someone (even you) makes a change to a file (or files) and makes those changes known to the revision control system, others with access to those files can not only see those changes, but integrate them into their own.

It provides a great deal of functionality which might appear to be complex and overwhelming.  Most of the functionality you will need in the basic daily use case is very narrow, so don't be discouraged by the depth and complexity of git's documentation.
 
### What's Git all about?
In revision control systems your code is typically stored in a **repository** and that repository  often lives and is managed on a remote server.  This is done for a variety of reasons, one if which is to provide others access to your code.  Git has the advantage of such code and its revisions being controlled locally and only when you're ready can those changes optionally be put onto the remote server.  The relationship between Git and Github is that Github provides a nice visual shell over Git and also serves as the remote git server, so you don't have to think about it when you want to share your code with others (or have a remote copy of it).

You will always need to install git on your local system, and don't ever _have to have_ a remote server, but if that is the case, the code in such a local project will never be seen by, or syncronized with (backed up on) a remote server, thus making it difficult to (though not technically impossible) share with others in the general case.

### Projects to Repositorities
In git your code lives in a repository.  This is simply the location/directory for your files and it lives (initially) local to your file system on your computer.  You can create a repository anywhere on your file system, but it is often a good practice to keep git repositories in a common location when it makes sense to do so.  Furthermore, there is no limit to the number of repositories or the number of files under the control of a repository.

You can consider a repository as a project containing a single focus of interest.  For example, you might think if your repository as containing a single complete software application you're building.  Similarly, you might think of it as a place for all the files of a single course over a semester, or a single topic of interest.  Your concept of "project" isn't really restricted, though there are some best practices.

In Github, as in git, the anchor of a project is the repository.

### Resources
* [Introductory videos on git](https://git-scm.com/videos)
* [Introductory guide on Github](https://guides.github.com/activities/hello-world/)

## Python

[Python](http://python.org) is among a few of the _de facto_ languages used in data mining, machine learning and data science broadly.

It has a simple, expressive syntax that is praised for its consistency and similarity to _psuedocode_, indeed, the syntax can be learned in a short time (usually a day or two) and because it is an interpreted language, beginners can be more productive because of the instant feedback and lack of complex compilation requirements of other languages.  Though Python is fantastic and widely loved, it is not without its criticisms, one of which being the complexity of its library ecosystem and the dual fork of the language (Python2 and Python3).

We will focus on Python3 as that is where the future of the language lives and also that support for Python2 is quickly waning, with official support ending by the decade's conclusion.

Instead of spending any time here going over Python, you'll be diverted to several good online resources for learning Python.

### The Python Data Science Stack

Python has a well developed ecosystem for doing data mining, machine learning and data science.  In fact, the language is well suited for many text manipulation tasks such as tokenizing, parsing and general data munging -- in just a few lines of code you can process a large text file, extracting from it a large corpus for post-processing.

There are five primary tools (in addition to Python) we'll use throughout  our data mining journey, Numpy, Pandas, SciPy and Scikit-Learn summarized in the table below.


| Tool | Summary |
|:----------:|:-------------------------------------|
|[Python](http://python.org)| we'll focus on Python 3|
|[NumPy](http://www.numpy.org/)| the primary library used for high performance data matrix operations  |
|[Pandas](http://pandas.pydata.org/)| the high level library of data structures used to make working with data a joyful experience|
|[Scikit-Learn](http://scikit-learn.org/stable/index.html)| the core machine learning and data mining library|
| [SciPy](https://docs.scipy.org/doc/scipy/reference/) |  the core scientific and numerical computing library, which we'll restrict our use to its statistical functions |
| [Jupter Notebooks/Lab](http://jupyter.org) | the primary tool for building code and data narratives [see below](#Jupyter-Notebooks) |

### Anaconda
While you can certainly install each of these separately (and it is perfectly OK to do so), it is advised that you breathe easier by installing this stack via [Anaconda](http://continuum.io/anaconda), which is becoming the _de facto_ packaging of the Python Data Science Stack.  It includes hundreds of the most popular Python libraries (including those listed above) and greatly simplifies the update, upgrade and dependency management required of all the packages in the distribution.  

## Jupyter Notebooks

### What?

In the last few years, Jupyter Notebooks have become one of several standard tools being used in data analysis and data science today. We will make heavy use of its features, but will begin with the basics.  So what is a Jupyter Notebook?

A Jupyter Notebook can be minimally summarized as :

* an _interactive_, _executable_ **document**, that
* _mixes code_ and _data_ with **narrative** (text, technical notes, etc.), that
* is _sharable_ and _editable_.


Think of your notebook as a way to explore data, while sharing the code along side your data exploration, while simultaneously having a conversation (through the narrative) describing the code, the data and the goal(s) you're trying to accomplish.

Jupyter is much more than described above, and certainly not the only tool out there, but it is one of the best at what it does and is getting better with each new version!

### Why?

In the scientific method, we often like to break the process down into the following rough steps:

1. formulate a question (from some general observation(s) / phenomenon)
2. propose a hypothesis that might explain the phenomenon
3. develop a prediction or model
4. gather data and test predictions / model
5. refine, alter, reject, expand hypothesis (and if necessary model)
6. **[iterate between steps 3-5]**
7. develop general theories from the outcomes

The scientific method works best when there is supporting documentation of each of these steps, because when sharing the outcomes of research, we are very much concerned with making sure our work is _repeatable_ and _reproducible_. Work is _repeatable_ when we execute the same methods on the same data and get the same result. It is _reproducible_ when we execute the same methods on new or different data and get results that are consistent with our theory or hypothesis. Both are necessary for good science. 

To make the "science" in "data science" relevant we will use the scientific method as our anchor. The power of Jupyter Notebooks is demonstrated in their flexibility to support nearly all computational and data-driven phases of the scientific method and hence data science. We can use the documentation and narrative building tools of the notebook to document our questions and hypotheses (1 and 2 above).  We can even link the documentation of our hypothesis to the original research being referenced or built upon.  Using the interactive programming paradigm of Jupyter (along side the documentation) we can test computations and build predictions and models in code, and even test early versions of those models interactively, perhaps even holding on to variations during iterative refinement.  

### How?

Data-driven analyses today can be considered a combination of explanatory narrative with computational support for that narrative.  With technology like Jupyter, we can marry the two so that they can co-exist together where they (arguably) make sense to.  

Jupyter supports narratives by introducing the concept of a "cell", where a cell _is a container for stuff_ ... that stuff being one of the following

* executing code (in a language like Python),
* plain text and Markdown, 
* math via \LaTeX mixed in with plain text and Markdown, or
* HTML.

What makes Jupyter different from other environments like Matlab is that cells containing executing code can be in a variety of supported languages.  While Python, R and Julia have robust support in Jupyter, other languages like Java, Javascript, FORTRAN and others can be included in a notebook.  Furthermore, a cell can support dynamic visualizations in HTML and Javascript, taking interactivity to another level. 

### Plain text narratives with Markdown

Jupyter cells that are designed for text can use a simple markup notation called [Markdown](https://daringfireball.net/projects/markdown/) and also \LaTeX for mathematical notation. Markdown is much like plain old text with a few simple notations for things like bold, italics, headings and linking.  In general, Markdown is not hard to learn and the more you use it the more natural it becomes.  The motivating philosophy behind it was to strive for readability, simplicity and unobtrusiveness in writing documentation.

We won't spend a lot of time here with Markdown as there are superb tutorials online to get you on your way.

### Math narratives with \LaTeX

[\LaTeX](http://www.latex-project.org) has been used for over  three decades to produce highly professional scientific documents and books.  It is likely you own at least one textbook (or course notes) that were written using \LaTeX, especially if the subject is math, physics or computer science.  One reason you may not have learned to use it, however, is that in general it has a high learning curve for beginners, and while the final output of a \LaTeX document is most certainly going to please, it may have taken much longer to produce your first version when compared to Google or Microsoft tools.

Luckily, Jupyter makes this much easier by removing the need for any complex formatting, and instead just supporting Markdown, while at the same time providing a great deal of support for the bulk of moderately complex \LaTeX math without much of the fancy typesetting that brings beginners to cut their losses and quit before a final product can be realized.  Breath easy, this will not be as difficult as may seem.

If you need to build narratives that are math heavy, Jupyter support for basic mathematical notation is built in to help you build nice looking documents (with _beautifully_ typeset math) that could _theoretically_ be exported to PDF and look almost as nice as a document written in a word processing environment like Google Docs or Microsoft Word (or even full \LaTeX).  While admittedly lacking many of the features of a "word processor", for computational narratives the Jupyter environment is compelling and the [Jupyter Lab](https://github.com/jupyterlab/jupyterlab) product promises even greater features and integrations.

Mathematical narratives in Jupyter can be useful in many contexts, for example,

* to explain a theoretical result or show the usage of a specific mathematical technique,
* to provide a mathematical proof of a result that you are deriving,
* to show the mathematical underpinnings of an algorithm, 
* to show the formulae used in a concrete calculation or manipulation of data.


Here are a few  math examples (view the source code for this notebook to see how easily it can be done):

Suppose that,
$$
f'(x) = { \lim_{ \Delta x \rightarrow 0 }  { { f(x + \Delta x) - f(x) } \over \Delta x } }
$$


and maybe
$$
\int x^n dx = { {x^{n+1}} \over n+1 } 
$$
therefore we have
$$
\sum_{k}^\infty { {t^k \over k!} = e^t }
$$

and in rare cases
$$
\sum_{\substack{
   0<i<m \\
   0<j<n
  }} 
 P(i,j).
$$

But we must consider the following cases

$$ f(n) =
  \begin{cases}
    n \over 2       & \quad \text{if } n \text{ is even}\\
    -(n+1) \over 2  & \quad \text{if } n \text{ is odd}\\
  \end{cases}
$$

and in cases where we can't, we might use

$$
A_{m,n} = 
 \begin{pmatrix}
  a_{1,1} & a_{1,2} & \cdots & a_{1,n} \\
  a_{2,1} & a_{2,2} & \cdots & a_{2,n} \\
  \vdots  & \vdots  & \ddots & \vdots  \\
  a_{m,1} & a_{m,2} & \cdots & a_{m,n} 
 \end{pmatrix}.
$$



But alas, we will end with some Greek

$$\alpha, \beta, \gamma, \kappa, \Pi, \Upsilon, \Omega, \ldots$$

Once you get the hang of developing narratives, you might never look back and wonder how you lived without these tools.  Here are some additional resources for using \LaTeX:

* this [Math Wiki](https://en.wikibooks.org/wiki/LaTeX/Mathematics) for \LaTeX has a nice summary of common math patterns,
* the \LaTeX [Cheatsheet](https://wch.github.io/latexsheet/latexsheet.pdf) is an indispensable tool that summarizes a lot of the macros in a printable two-pager, bookmark it ... it is your friend for life if you go deeper into using it!

### Code narratives

The strength of Jupyter is apparent, when looking at what it can do to help you build interactive documents that aim to support computational work. Let's just work through a real example ... where we will:

* get USGS earthquake data,
* explore this data for the highest magnitude earthquakes (let's say the top 10)
* put those earthquakes on an interactive map.

**A Data Exploration of Earthquakes**

Let's say we are interested in programmatically obtaining the largest earthquakes in the 2016.

Luckily the [USGS has an API](https://earthquake.usgs.gov/fdsnws/event/1/) to do most of the heavy lifting for.  We simply need to create a query to the service to ask for all the earthquakes of magnitude 7 or greater in 2016 and then we'll filter them on some additional magnitude criterion on our own.


```python
import requests
r = requests.get("https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&starttime=2016-01-01&endtime=2017-01-01&minmagnitude=7")
```

Let's store the data in a variable named `data`:


```python
data = r.json()
```

And quickly inspect it (it should be in [GeoJSON](http://geojson.org)) ...


```python
print(data) # yup, looks like GeoJSON
```

    {'type': 'FeatureCollection', 'metadata': {'generated': 1503769335000, 'url': 'https://earthquake.usgs.gov/fdsnws/event/1/query?format=geojson&starttime=2016-01-01&endtime=2017-01-01&minmagnitude=7', 'title': 'USGS Earthquakes', 'status': 200, 'api': '1.5.8', 'count': 16}, 'features': [{'type': 'Feature', 'properties': {'mag': 7.6, 'place': '41km SW of Puerto Quellon, Chile', 'time': 1482675747010, 'updated': 1490309522040, 'tz': -240, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us10007mn3', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us10007mn3&format=geojson', 'felt': 265, 'cdi': 9.1, 'mmi': 7.8, 'alert': 'yellow', 'status': 'reviewed', 'tsunami': 1, 'sig': 1130, 'net': 'us', 'code': '10007mn3', 'ids': ',at00oiqvxe,pt16360050,us10007mn3,', 'sources': ',at,pt,us,', 'types': ',dyfi,finite-fault,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,origin,phase-data,poster,shakemap,', 'nst': None, 'dmin': 0.355, 'rms': 0.79, 'gap': 29, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.6 - 41km SW of Puerto Quellon, Chile'}, 'geometry': {'type': 'Point', 'coordinates': [-73.9413, -43.4064, 38]}, 'id': 'us10007mn3'}, {'type': 'Feature', 'properties': {'mag': 7.9, 'place': '54km E of Taron, Papua New Guinea', 'time': 1481971870500, 'updated': 1489631484040, 'tz': 600, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us200081v8', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us200081v8&format=geojson', 'felt': 15, 'cdi': 8.7, 'mmi': 8.1, 'alert': 'yellow', 'status': 'reviewed', 'tsunami': 1, 'sig': 973, 'net': 'us', 'code': '200081v8', 'ids': ',pt16352050,us200081v8,at00oibstb,', 'sources': ',pt,us,at,', 'types': ',dyfi,finite-fault,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,origin,phase-data,poster,shakemap,', 'nst': None, 'dmin': 1.389, 'rms': 0.97, 'gap': 13, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.9 - 54km E of Taron, Papua New Guinea'}, 'geometry': {'type': 'Point', 'coordinates': [153.5216, -4.5049, 94.54]}, 'id': 'us200081v8'}, {'type': 'Feature', 'properties': {'mag': 7.8, 'place': '69km WSW of Kirakira, Solomon Islands', 'time': 1481218726280, 'updated': 1488524768040, 'tz': 660, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us20007z80', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us20007z80&format=geojson', 'felt': 28, 'cdi': 9.1, 'mmi': 7.82, 'alert': 'green', 'status': 'reviewed', 'tsunami': 1, 'sig': 961, 'net': 'us', 'code': '20007z80', 'ids': ',at00ohvnon,us20007z80,pt16343053,', 'sources': ',at,us,pt,', 'types': ',dyfi,finite-fault,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,origin,phase-data,poster,shakemap,', 'nst': None, 'dmin': 1.836, 'rms': 0.88, 'gap': 13, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.8 - 69km WSW of Kirakira, Solomon Islands'}, 'geometry': {'type': 'Point', 'coordinates': [161.3273, -10.6812, 40]}, 'id': 'us20007z80'}, {'type': 'Feature', 'properties': {'mag': 7.8, 'place': '54km NNE of Amberley, New Zealand', 'time': 1479034976340, 'updated': 1486883416123, 'tz': 720, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us1000778i', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us1000778i&format=geojson', 'felt': 708, 'cdi': 9.1, 'mmi': 8.85, 'alert': 'orange', 'status': 'reviewed', 'tsunami': 1, 'sig': 1644, 'net': 'us', 'code': '1000778i', 'ids': ',at00ogkuoy,us1000778i,', 'sources': ',at,us,', 'types': ',cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,origin,phase-data,poster,scitech-link,shakemap,', 'nst': None, 'dmin': 0.481, 'rms': 0.56, 'gap': 21, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.8 - 54km NNE of Amberley, New Zealand'}, 'geometry': {'type': 'Point', 'coordinates': [173.054, -42.7373, 15.11]}, 'id': 'us1000778i'}, {'type': 'Feature', 'properties': {'mag': 7, 'place': '175km NE of Gisborne, New Zealand', 'time': 1472747877300, 'updated': 1486511457758, 'tz': 720, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us10006jbi', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us10006jbi&format=geojson', 'felt': 292, 'cdi': 4.9, 'mmi': 6.11, 'alert': 'green', 'status': 'reviewed', 'tsunami': 1, 'sig': 897, 'net': 'us', 'code': '10006jbi', 'ids': ',at00ocu3ja,pt16245050,us10006jbi,gcmt20160901163757,', 'sources': ',at,pt,us,gcmt,', 'types': ',cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,origin,phase-data,poster,shakemap,', 'nst': None, 'dmin': 0.698, 'rms': 0.88, 'gap': 21, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.0 - 175km NE of Gisborne, New Zealand'}, 'geometry': {'type': 'Point', 'coordinates': [179.1461, -37.3586, 19]}, 'id': 'us10006jbi'}, {'type': 'Feature', 'properties': {'mag': 7.1, 'place': 'North of Ascension Island', 'time': 1472444997860, 'updated': 1486511450814, 'tz': -60, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us20006uy6', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us20006uy6&format=geojson', 'felt': 8, 'cdi': 3.4, 'mmi': 0, 'alert': 'green', 'status': 'reviewed', 'tsunami': 1, 'sig': 778, 'net': 'us', 'code': '20006uy6', 'ids': ',at00ocnltz,us20006uy6,gcmt20160829042957,', 'sources': ',at,us,gcmt,', 'types': ',cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,origin,phase-data,poster,shakemap,', 'nst': None, 'dmin': 8.561, 'rms': 0.87, 'gap': 24, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.1 - North of Ascension Island'}, 'geometry': {'type': 'Point', 'coordinates': [-17.8255, -0.0456, 10]}, 'id': 'us20006uy6'}, {'type': 'Feature', 'properties': {'mag': 7.4, 'place': 'South Georgia Island region', 'time': 1471591942710, 'updated': 1486511443677, 'tz': -120, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us10006exl', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us10006exl&format=geojson', 'felt': 1, 'cdi': 2.7, 'mmi': 0, 'alert': 'green', 'status': 'reviewed', 'tsunami': 0, 'sig': 843, 'net': 'us', 'code': '10006exl', 'ids': ',us10006exl,gcmt20160819073222,', 'sources': ',us,gcmt,', 'types': ',cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-text,losspager,moment-tensor,origin,phase-data,poster,shakemap,', 'nst': None, 'dmin': 2.852, 'rms': 0.79, 'gap': 18, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.4 - South Georgia Island region'}, 'geometry': {'type': 'Point', 'coordinates': [-31.8766, -55.2852, 10]}, 'id': 'us10006exl'}, {'type': 'Feature', 'properties': {'mag': 7.2, 'place': '110km E of Ile Hunter, New Caledonia', 'time': 1470965196280, 'updated': 1486511438119, 'tz': 720, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us10006d5h', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us10006d5h&format=geojson', 'felt': 2, 'cdi': 6.2, 'mmi': 5.1, 'alert': 'green', 'status': 'reviewed', 'tsunami': 1, 'sig': 799, 'net': 'us', 'code': '10006d5h', 'ids': ',at00obrw0f,pt16225050,us10006d5h,gcmt20160812012635,', 'sources': ',at,pt,us,gcmt,', 'types': ',cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,origin,phase-data,poster,shakemap,', 'nst': None, 'dmin': 4.823, 'rms': 0.9, 'gap': 14, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.2 - 110km E of Ile Hunter, New Caledonia'}, 'geometry': {'type': 'Point', 'coordinates': [173.1167, -22.4765, 16.37]}, 'id': 'us10006d5h'}, {'type': 'Feature', 'properties': {'mag': 7.7, 'place': '29km SW of Agrihan, Northern Mariana Islands', 'time': 1469827104740, 'updated': 1486511415901, 'tz': 600, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us100068jg', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us100068jg&format=geojson', 'felt': 129, 'cdi': 4.6, 'mmi': 6.33, 'alert': 'green', 'status': 'reviewed', 'tsunami': 1, 'sig': 971, 'net': 'us', 'code': '100068jg', 'ids': ',at00ob3huo,us100068jg,gcmt20160729211825,', 'sources': ',at,us,gcmt,', 'types': ',cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,nearby-cities,origin,phase-data,poster,shakemap,tectonic-summary,', 'nst': None, 'dmin': 3.294, 'rms': 1.38, 'gap': 14, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.7 - 29km SW of Agrihan, Northern Mariana Islands'}, 'geometry': {'type': 'Point', 'coordinates': [145.5073, 18.5429, 196]}, 'id': 'us100068jg'}, {'type': 'Feature', 'properties': {'mag': 7.2, 'place': '53km NNE of Visokoi Island, South Georgia and the South Sandwich Islands', 'time': 1464428819780, 'updated': 1486511394060, 'tz': -120, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us20005ysu', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us20005ysu&format=geojson', 'felt': 0, 'cdi': 1, 'mmi': 6.01, 'alert': 'green', 'status': 'reviewed', 'tsunami': 1, 'sig': 798, 'net': 'us', 'code': '20005ysu', 'ids': ',at00o7vsif,us20005ysu,gcmt20160528094659,', 'sources': ',at,us,gcmt,', 'types': ',cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-link,losspager,moment-tensor,nearby-cities,origin,phase-data,poster,shakemap,', 'nst': None, 'dmin': 5.803, 'rms': 0.89, 'gap': 24, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.2 - 53km NNE of Visokoi Island, South Georgia and the South Sandwich Islands'}, 'geometry': {'type': 'Point', 'coordinates': [-26.9353, -56.2409, 78]}, 'id': 'us20005ysu'}, {'type': 'Feature', 'properties': {'mag': 7, 'place': '2km N of Norsup, Vanuatu', 'time': 1461872004070, 'updated': 1486511387232, 'tz': 660, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us10005c88', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us10005c88&format=geojson', 'felt': 2, 'cdi': 6.8, 'mmi': 6.5, 'alert': 'green', 'status': 'reviewed', 'tsunami': 1, 'sig': 755, 'net': 'us', 'code': '10005c88', 'ids': ',pt16119051,at00o6cznp,us10005c88,gcmt20160428193324,', 'sources': ',pt,at,us,gcmt,', 'types': ',cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,nearby-cities,origin,phase-data,poster,shakemap,tectonic-summary,trump-moment-tensor,', 'nst': None, 'dmin': 0.616, 'rms': 1.33, 'gap': 14, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.0 - 2km N of Norsup, Vanuatu'}, 'geometry': {'type': 'Point', 'coordinates': [167.3786, -16.0429, 24]}, 'id': 'us10005c88'}, {'type': 'Feature', 'properties': {'mag': 7.8, 'place': '27km SSE of Muisne, Ecuador', 'time': 1460851116980, 'updated': 1497458054864, 'tz': -300, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us20005j32', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us20005j32&format=geojson', 'felt': 193, 'cdi': 9.1, 'mmi': 8.08, 'alert': 'orange', 'status': 'reviewed', 'tsunami': 1, 'sig': 1176, 'net': 'us', 'code': '20005j32', 'ids': ',at00o5r3xd,us20005j32,pt16107050,gcmt20160416235837,', 'sources': ',at,us,pt,gcmt,', 'types': ',cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,nearby-cities,origin,phase-data,poster,shakemap,tectonic-summary,', 'nst': None, 'dmin': 1.44, 'rms': 0.94, 'gap': 15, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.8 - 27km SSE of Muisne, Ecuador'}, 'geometry': {'type': 'Point', 'coordinates': [-79.9218, 0.3819, 20.59]}, 'id': 'us20005j32'}, {'type': 'Feature', 'properties': {'mag': 7, 'place': '1km E of Kumamoto-shi, Japan', 'time': 1460737506220, 'updated': 1496584613178, 'tz': 540, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us20005iis', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us20005iis&format=geojson', 'felt': 72, 'cdi': 8.4, 'mmi': 9.3, 'alert': 'red', 'status': 'reviewed', 'tsunami': 1, 'sig': 2060, 'net': 'us', 'code': '20005iis', 'ids': ',at00o5oo9v,pt16106053,us20005iis,gcmt20160415162506,', 'sources': ',at,pt,us,gcmt,', 'types': ',cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,nearby-cities,origin,phase-data,poster,scitech-link,shakemap,tectonic-summary,', 'nst': None, 'dmin': 0.349, 'rms': 0.85, 'gap': 32, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.0 - 1km E of Kumamoto-shi, Japan'}, 'geometry': {'type': 'Point', 'coordinates': [130.7543, 32.7906, 10]}, 'id': 'us20005iis'}, {'type': 'Feature', 'properties': {'mag': 7.8, 'place': 'Southwest of Sumatra, Indonesia', 'time': 1456922988110, 'updated': 1486511353268, 'tz': 360, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us10004u1y', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us10004u1y&format=geojson', 'felt': 30, 'cdi': 3.8, 'mmi': 3.07, 'alert': 'green', 'status': 'reviewed', 'tsunami': 1, 'sig': 947, 'net': 'us', 'code': '10004u1y', 'ids': ',us10004u1y,gcmt20160302124948,', 'sources': ',us,gcmt,', 'types': ',dyfi,finite-fault,general-link,general-text,geoserve,impact-text,losspager,moment-tensor,nearby-cities,origin,phase-data,poster,shakemap,tectonic-summary,', 'nst': None, 'dmin': 7.009, 'rms': 1.14, 'gap': 20, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.8 - Southwest of Sumatra, Indonesia'}, 'geometry': {'type': 'Point', 'coordinates': [94.3299, -4.9521, 24]}, 'id': 'us10004u1y'}, {'type': 'Feature', 'properties': {'mag': 7.2, 'place': '88km N of Yelizovo, Russia', 'time': 1454124312220, 'updated': 1486511313778, 'tz': 720, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us20004vvx', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us20004vvx&format=geojson', 'felt': 2, 'cdi': 3.4, 'mmi': 5.82, 'alert': 'green', 'status': 'reviewed', 'tsunami': 1, 'sig': 798, 'net': 'us', 'code': '20004vvx', 'ids': ',gcmt20160130032510,at00o1qxho,pt16030050,us20004vvx,gcmt20160130032512,', 'sources': ',gcmt,at,pt,us,gcmt,', 'types': ',associate,cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,nearby-cities,origin,phase-data,shakemap,tectonic-summary,', 'nst': None, 'dmin': 0.958, 'rms': 1.19, 'gap': 17, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.2 - 88km N of Yelizovo, Russia'}, 'geometry': {'type': 'Point', 'coordinates': [158.5463, 53.9776, 177]}, 'id': 'us20004vvx'}, {'type': 'Feature', 'properties': {'mag': 7.1, 'place': '86km E of Old Iliamna, Alaska', 'time': 1453631430230, 'updated': 1486511256806, 'tz': -540, 'url': 'https://earthquake.usgs.gov/earthquakes/eventpage/us10004gqp', 'detail': 'https://earthquake.usgs.gov/fdsnws/event/1/query?eventid=us10004gqp&format=geojson', 'felt': 1816, 'cdi': 7.2, 'mmi': 6.6, 'alert': 'green', 'status': 'reviewed', 'tsunami': 1, 'sig': 1496, 'net': 'us', 'code': '10004gqp', 'ids': ',at00o1gd6r,us10004gqp,ak12496371,gcmt20160124103030,', 'sources': ',at,us,ak,gcmt,', 'types': ',cap,dyfi,finite-fault,general-link,general-text,geoserve,impact-link,impact-text,losspager,moment-tensor,nearby-cities,origin,phase-data,shakemap,tectonic-summary,trump-origin,', 'nst': None, 'dmin': 0.72, 'rms': 2.11, 'gap': 19, 'magType': 'mww', 'type': 'earthquake', 'title': 'M 7.1 - 86km E of Old Iliamna, Alaska'}, 'geometry': {'type': 'Point', 'coordinates': [-153.4051, 59.6363, 129]}, 'id': 'us10004gqp'}], 'bbox': [-153.4051, -56.2409, 10, 179.1461, 59.6363, 196]}
    

Without going into tremendous detail here, we would like to iterate over this data and grab the following information:

* the **magnitude** of the earthquake,
* the **USGS location name** of that place (in English), and 
* the **lat/lon coordinates** so we can plot on the map.

**ALL** of this information is in our `data` object, so let's get to it:


```python
for f in data['features']:
    place = f['properties']['place']
    magnitude = f['properties']['mag']
    lat, lon, z = f['geometry']['coordinates']
    
    print("{}\t{}\t{}\t{}".format(place, magnitude, lat, lon))
```

    41km SW of Puerto Quellon, Chile	7.6	-73.9413	-43.4064
    54km E of Taron, Papua New Guinea	7.9	153.5216	-4.5049
    69km WSW of Kirakira, Solomon Islands	7.8	161.3273	-10.6812
    54km NNE of Amberley, New Zealand	7.8	173.054	-42.7373
    175km NE of Gisborne, New Zealand	7	179.1461	-37.3586
    North of Ascension Island	7.1	-17.8255	-0.0456
    South Georgia Island region	7.4	-31.8766	-55.2852
    110km E of Ile Hunter, New Caledonia	7.2	173.1167	-22.4765
    29km SW of Agrihan, Northern Mariana Islands	7.7	145.5073	18.5429
    53km NNE of Visokoi Island, South Georgia and the South Sandwich Islands	7.2	-26.9353	-56.2409
    2km N of Norsup, Vanuatu	7	167.3786	-16.0429
    27km SSE of Muisne, Ecuador	7.8	-79.9218	0.3819
    1km E of Kumamoto-shi, Japan	7	130.7543	32.7906
    Southwest of Sumatra, Indonesia	7.8	94.3299	-4.9521
    88km N of Yelizovo, Russia	7.2	158.5463	53.9776
    86km E of Old Iliamna, Alaska	7.1	-153.4051	59.6363
    

For the purposes of our demo, we need not store this information in any special way.  We'll return to the data and our final task of plotting this on an _interactive_ map.  We'll use the library [folium](https://folium.readthedocs.io/en/latest/) to get the trick done as easily as possible.


```python
import folium
map_eq = folium.Map(location=[37.733795, -122.446747], zoom_start=2)
```


```python
for f in data['features']:
    place = f['properties']['place']
    magnitude = f['properties']['mag']
    lat, lon, z = f['geometry']['coordinates']

    # place the data on the map!
    folium.Marker([lon, lat], popup='place:{}\nmagnitude:{}'.format(place, magnitude)).add_to(map_eq)
map_eq
```




<div style="width:100%;"><div style="position:relative;width:100%;height:0;padding-bottom:60%;"><iframe src="data:text/html;charset=utf-8;base64,PCFET0NUWVBFIGh0bWw+CjxoZWFkPiAgICAKICAgIDxtZXRhIGh0dHAtZXF1aXY9ImNvbnRlbnQtdHlwZSIgY29udGVudD0idGV4dC9odG1sOyBjaGFyc2V0PVVURi04IiAvPgogICAgPHNjcmlwdD5MX1BSRUZFUl9DQU5WQVMgPSBmYWxzZTsgTF9OT19UT1VDSCA9IGZhbHNlOyBMX0RJU0FCTEVfM0QgPSBmYWxzZTs8L3NjcmlwdD4KICAgIDxzY3JpcHQgc3JjPSJodHRwczovL3VucGtnLmNvbS9sZWFmbGV0QDEuMC4xL2Rpc3QvbGVhZmxldC5qcyI+PC9zY3JpcHQ+CiAgICA8c2NyaXB0IHNyYz0iaHR0cHM6Ly9hamF4Lmdvb2dsZWFwaXMuY29tL2FqYXgvbGlicy9qcXVlcnkvMS4xMS4xL2pxdWVyeS5taW4uanMiPjwvc2NyaXB0PgogICAgPHNjcmlwdCBzcmM9Imh0dHBzOi8vbWF4Y2RuLmJvb3RzdHJhcGNkbi5jb20vYm9vdHN0cmFwLzMuMi4wL2pzL2Jvb3RzdHJhcC5taW4uanMiPjwvc2NyaXB0PgogICAgPHNjcmlwdCBzcmM9Imh0dHBzOi8vY2RuanMuY2xvdWRmbGFyZS5jb20vYWpheC9saWJzL0xlYWZsZXQuYXdlc29tZS1tYXJrZXJzLzIuMC4yL2xlYWZsZXQuYXdlc29tZS1tYXJrZXJzLmpzIj48L3NjcmlwdD4KICAgIDxzY3JpcHQgc3JjPSJodHRwczovL2NkbmpzLmNsb3VkZmxhcmUuY29tL2FqYXgvbGlicy9sZWFmbGV0Lm1hcmtlcmNsdXN0ZXIvMS4wLjAvbGVhZmxldC5tYXJrZXJjbHVzdGVyLXNyYy5qcyI+PC9zY3JpcHQ+CiAgICA8c2NyaXB0IHNyYz0iaHR0cHM6Ly9jZG5qcy5jbG91ZGZsYXJlLmNvbS9hamF4L2xpYnMvbGVhZmxldC5tYXJrZXJjbHVzdGVyLzEuMC4wL2xlYWZsZXQubWFya2VyY2x1c3Rlci5qcyI+PC9zY3JpcHQ+CiAgICA8bGluayByZWw9InN0eWxlc2hlZXQiIGhyZWY9Imh0dHBzOi8vdW5wa2cuY29tL2xlYWZsZXRAMS4wLjEvZGlzdC9sZWFmbGV0LmNzcyIgLz4KICAgIDxsaW5rIHJlbD0ic3R5bGVzaGVldCIgaHJlZj0iaHR0cHM6Ly9tYXhjZG4uYm9vdHN0cmFwY2RuLmNvbS9ib290c3RyYXAvMy4yLjAvY3NzL2Jvb3RzdHJhcC5taW4uY3NzIiAvPgogICAgPGxpbmsgcmVsPSJzdHlsZXNoZWV0IiBocmVmPSJodHRwczovL21heGNkbi5ib290c3RyYXBjZG4uY29tL2Jvb3RzdHJhcC8zLjIuMC9jc3MvYm9vdHN0cmFwLXRoZW1lLm1pbi5jc3MiIC8+CiAgICA8bGluayByZWw9InN0eWxlc2hlZXQiIGhyZWY9Imh0dHBzOi8vbWF4Y2RuLmJvb3RzdHJhcGNkbi5jb20vZm9udC1hd2Vzb21lLzQuNi4zL2Nzcy9mb250LWF3ZXNvbWUubWluLmNzcyIgLz4KICAgIDxsaW5rIHJlbD0ic3R5bGVzaGVldCIgaHJlZj0iaHR0cHM6Ly9jZG5qcy5jbG91ZGZsYXJlLmNvbS9hamF4L2xpYnMvTGVhZmxldC5hd2Vzb21lLW1hcmtlcnMvMi4wLjIvbGVhZmxldC5hd2Vzb21lLW1hcmtlcnMuY3NzIiAvPgogICAgPGxpbmsgcmVsPSJzdHlsZXNoZWV0IiBocmVmPSJodHRwczovL2NkbmpzLmNsb3VkZmxhcmUuY29tL2FqYXgvbGlicy9sZWFmbGV0Lm1hcmtlcmNsdXN0ZXIvMS4wLjAvTWFya2VyQ2x1c3Rlci5EZWZhdWx0LmNzcyIgLz4KICAgIDxsaW5rIHJlbD0ic3R5bGVzaGVldCIgaHJlZj0iaHR0cHM6Ly9jZG5qcy5jbG91ZGZsYXJlLmNvbS9hamF4L2xpYnMvbGVhZmxldC5tYXJrZXJjbHVzdGVyLzEuMC4wL01hcmtlckNsdXN0ZXIuY3NzIiAvPgogICAgPGxpbmsgcmVsPSJzdHlsZXNoZWV0IiBocmVmPSJodHRwczovL3Jhd2dpdC5jb20vcHl0aG9uLXZpc3VhbGl6YXRpb24vZm9saXVtL21hc3Rlci9mb2xpdW0vdGVtcGxhdGVzL2xlYWZsZXQuYXdlc29tZS5yb3RhdGUuY3NzIiAvPgogICAgPHN0eWxlPmh0bWwsIGJvZHkge3dpZHRoOiAxMDAlO2hlaWdodDogMTAwJTttYXJnaW46IDA7cGFkZGluZzogMDt9PC9zdHlsZT4KICAgIDxzdHlsZT4jbWFwIHtwb3NpdGlvbjphYnNvbHV0ZTt0b3A6MDtib3R0b206MDtyaWdodDowO2xlZnQ6MDt9PC9zdHlsZT4KICAgIAogICAgICAgICAgICA8c3R5bGU+ICNtYXBfYTA2ZjljNzg4ZGYwNDNjMTk0YmU1OTU2Zjk5YTZkMDUgewogICAgICAgICAgICAgICAgcG9zaXRpb24gOiByZWxhdGl2ZTsKICAgICAgICAgICAgICAgIHdpZHRoIDogMTAwLjAlOwogICAgICAgICAgICAgICAgaGVpZ2h0OiAxMDAuMCU7CiAgICAgICAgICAgICAgICBsZWZ0OiAwLjAlOwogICAgICAgICAgICAgICAgdG9wOiAwLjAlOwogICAgICAgICAgICAgICAgfQogICAgICAgICAgICA8L3N0eWxlPgogICAgICAgIAo8L2hlYWQ+Cjxib2R5PiAgICAKICAgIAogICAgICAgICAgICA8ZGl2IGNsYXNzPSJmb2xpdW0tbWFwIiBpZD0ibWFwX2EwNmY5Yzc4OGRmMDQzYzE5NGJlNTk1NmY5OWE2ZDA1IiA+PC9kaXY+CiAgICAgICAgCjwvYm9keT4KPHNjcmlwdD4gICAgCiAgICAKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIHNvdXRoV2VzdCA9IEwubGF0TG5nKC05MCwgLTE4MCk7CiAgICAgICAgICAgICAgICB2YXIgbm9ydGhFYXN0ID0gTC5sYXRMbmcoOTAsIDE4MCk7CiAgICAgICAgICAgICAgICB2YXIgYm91bmRzID0gTC5sYXRMbmdCb3VuZHMoc291dGhXZXN0LCBub3J0aEVhc3QpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIHZhciBtYXBfYTA2ZjljNzg4ZGYwNDNjMTk0YmU1OTU2Zjk5YTZkMDUgPSBMLm1hcCgKICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICdtYXBfYTA2ZjljNzg4ZGYwNDNjMTk0YmU1OTU2Zjk5YTZkMDUnLAogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAge2NlbnRlcjogWzM3LjczMzc5NSwtMTIyLjQ0Njc0N10sCiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICB6b29tOiAyLAogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgbWF4Qm91bmRzOiBib3VuZHMsCiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICBsYXllcnM6IFtdLAogICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgd29ybGRDb3B5SnVtcDogZmFsc2UsCiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICBjcnM6IEwuQ1JTLkVQU0czODU3CiAgICAgICAgICAgICAgICAgICAgICAgICAgICAgICAgIH0pOwogICAgICAgICAgICAKICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgdGlsZV9sYXllcl9jY2UwMmI5ZjFjM2I0OGQ1OTM0MTA1ODdkNjgzOWQwZCA9IEwudGlsZUxheWVyKAogICAgICAgICAgICAgICAgJ2h0dHBzOi8ve3N9LnRpbGUub3BlbnN0cmVldG1hcC5vcmcve3p9L3t4fS97eX0ucG5nJywKICAgICAgICAgICAgICAgIHsKICAgICAgICAgICAgICAgICAgICBtYXhab29tOiAxOCwKICAgICAgICAgICAgICAgICAgICBtaW5ab29tOiAxLAogICAgICAgICAgICAgICAgICAgIGNvbnRpbnVvdXNXb3JsZDogZmFsc2UsCiAgICAgICAgICAgICAgICAgICAgbm9XcmFwOiBmYWxzZSwKICAgICAgICAgICAgICAgICAgICBhdHRyaWJ1dGlvbjogJ0RhdGEgYnkgPGEgaHJlZj0iaHR0cDovL29wZW5zdHJlZXRtYXAub3JnIj5PcGVuU3RyZWV0TWFwPC9hPiwgdW5kZXIgPGEgaHJlZj0iaHR0cDovL3d3dy5vcGVuc3RyZWV0bWFwLm9yZy9jb3B5cmlnaHQiPk9EYkw8L2E+LicsCiAgICAgICAgICAgICAgICAgICAgZGV0ZWN0UmV0aW5hOiBmYWxzZQogICAgICAgICAgICAgICAgICAgIH0KICAgICAgICAgICAgICAgICkuYWRkVG8obWFwX2EwNmY5Yzc4OGRmMDQzYzE5NGJlNTk1NmY5OWE2ZDA1KTsKCiAgICAgICAgCiAgICAKCiAgICAgICAgICAgIHZhciBtYXJrZXJfOGY5NGI5NGU2ZTMyNDk0Nzg1ZTMzMWZmYjdmMzgxNWQgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFstNDMuNDA2NCwtNzMuOTQxM10sCiAgICAgICAgICAgICAgICB7CiAgICAgICAgICAgICAgICAgICAgaWNvbjogbmV3IEwuSWNvbi5EZWZhdWx0KCkKICAgICAgICAgICAgICAgICAgICB9CiAgICAgICAgICAgICAgICApCiAgICAgICAgICAgICAgICAuYWRkVG8obWFwX2EwNmY5Yzc4OGRmMDQzYzE5NGJlNTk1NmY5OWE2ZDA1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzIzYmMxNWY1N2ZiNjQ5M2I4OTZiNzg1YWM2Zjg1ZDg3ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzBjNGU0ZTUyNjk4ZjRjZDFiN2M5M2U2YjJmZTZhYjRkID0gJCgnPGRpdiBpZD0iaHRtbF8wYzRlNGU1MjY5OGY0Y2QxYjdjOTNlNmIyZmU2YWI0ZCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+cGxhY2U6NDFrbSBTVyBvZiBQdWVydG8gUXVlbGxvbiwgQ2hpbGUgbWFnbml0dWRlOjcuNjwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMjNiYzE1ZjU3ZmI2NDkzYjg5NmI3ODVhYzZmODVkODcuc2V0Q29udGVudChodG1sXzBjNGU0ZTUyNjk4ZjRjZDFiN2M5M2U2YjJmZTZhYjRkKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBtYXJrZXJfOGY5NGI5NGU2ZTMyNDk0Nzg1ZTMzMWZmYjdmMzgxNWQuYmluZFBvcHVwKHBvcHVwXzIzYmMxNWY1N2ZiNjQ5M2I4OTZiNzg1YWM2Zjg1ZDg3KTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCgogICAgICAgICAgICB2YXIgbWFya2VyX2FjZDg4ZmMzMjNjOTRlNjBiN2RmMmQyYmNhNGZjMjMwID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbLTQuNTA0OSwxNTMuNTIxNl0sCiAgICAgICAgICAgICAgICB7CiAgICAgICAgICAgICAgICAgICAgaWNvbjogbmV3IEwuSWNvbi5EZWZhdWx0KCkKICAgICAgICAgICAgICAgICAgICB9CiAgICAgICAgICAgICAgICApCiAgICAgICAgICAgICAgICAuYWRkVG8obWFwX2EwNmY5Yzc4OGRmMDQzYzE5NGJlNTk1NmY5OWE2ZDA1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzIwNTk1NTI5M2JjMDQ5MzliZDMyNGE5MWQzM2U4OWE2ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2YzM2M3MWMzMTA4ZTQwNGJiN2Y2MTAzMTkxMDczYzVkID0gJCgnPGRpdiBpZD0iaHRtbF9mMzNjNzFjMzEwOGU0MDRiYjdmNjEwMzE5MTA3M2M1ZCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+cGxhY2U6NTRrbSBFIG9mIFRhcm9uLCBQYXB1YSBOZXcgR3VpbmVhIG1hZ25pdHVkZTo3Ljk8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzIwNTk1NTI5M2JjMDQ5MzliZDMyNGE5MWQzM2U4OWE2LnNldENvbnRlbnQoaHRtbF9mMzNjNzFjMzEwOGU0MDRiYjdmNjEwMzE5MTA3M2M1ZCk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgbWFya2VyX2FjZDg4ZmMzMjNjOTRlNjBiN2RmMmQyYmNhNGZjMjMwLmJpbmRQb3B1cChwb3B1cF8yMDU5NTUyOTNiYzA0OTM5YmQzMjRhOTFkMzNlODlhNik7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAoKICAgICAgICAgICAgdmFyIG1hcmtlcl9jODc1MmRiZGUyNDM0ODJkYWE2MjZlYjE0YmVjNzkyYSA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWy0xMC42ODEyLDE2MS4zMjczXSwKICAgICAgICAgICAgICAgIHsKICAgICAgICAgICAgICAgICAgICBpY29uOiBuZXcgTC5JY29uLkRlZmF1bHQoKQogICAgICAgICAgICAgICAgICAgIH0KICAgICAgICAgICAgICAgICkKICAgICAgICAgICAgICAgIC5hZGRUbyhtYXBfYTA2ZjljNzg4ZGYwNDNjMTk0YmU1OTU2Zjk5YTZkMDUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMjM3OTQ3ZTY3OGY2NGQzYTg4YzcxZTY1OTdlY2Q1NTMgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNzZlNjBjOTMzYzFlNGZiNjhjNTEwZmEzMzQxNWZmOTEgPSAkKCc8ZGl2IGlkPSJodG1sXzc2ZTYwYzkzM2MxZTRmYjY4YzUxMGZhMzM0MTVmZjkxIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5wbGFjZTo2OWttIFdTVyBvZiBLaXJha2lyYSwgU29sb21vbiBJc2xhbmRzIG1hZ25pdHVkZTo3Ljg8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzIzNzk0N2U2NzhmNjRkM2E4OGM3MWU2NTk3ZWNkNTUzLnNldENvbnRlbnQoaHRtbF83NmU2MGM5MzNjMWU0ZmI2OGM1MTBmYTMzNDE1ZmY5MSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgbWFya2VyX2M4NzUyZGJkZTI0MzQ4MmRhYTYyNmViMTRiZWM3OTJhLmJpbmRQb3B1cChwb3B1cF8yMzc5NDdlNjc4ZjY0ZDNhODhjNzFlNjU5N2VjZDU1Myk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAoKICAgICAgICAgICAgdmFyIG1hcmtlcl9jN2EzYTk0ZWMzMzk0NzExYWJkMDMwMjNjYjNkMTllZSA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWy00Mi43MzczLDE3My4wNTRdLAogICAgICAgICAgICAgICAgewogICAgICAgICAgICAgICAgICAgIGljb246IG5ldyBMLkljb24uRGVmYXVsdCgpCiAgICAgICAgICAgICAgICAgICAgfQogICAgICAgICAgICAgICAgKQogICAgICAgICAgICAgICAgLmFkZFRvKG1hcF9hMDZmOWM3ODhkZjA0M2MxOTRiZTU5NTZmOTlhNmQwNSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9kNTQyNDMzYWZhYjM0MmM1OWE3NWRmNTI0OTQzZjU2YiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF80YmE2ODFmZTA2Yzg0YjFhYTkwOGQ2YWI3ZjM0YjA1NSA9ICQoJzxkaXYgaWQ9Imh0bWxfNGJhNjgxZmUwNmM4NGIxYWE5MDhkNmFiN2YzNGIwNTUiIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPnBsYWNlOjU0a20gTk5FIG9mIEFtYmVybGV5LCBOZXcgWmVhbGFuZCBtYWduaXR1ZGU6Ny44PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9kNTQyNDMzYWZhYjM0MmM1OWE3NWRmNTI0OTQzZjU2Yi5zZXRDb250ZW50KGh0bWxfNGJhNjgxZmUwNmM4NGIxYWE5MDhkNmFiN2YzNGIwNTUpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIG1hcmtlcl9jN2EzYTk0ZWMzMzk0NzExYWJkMDMwMjNjYjNkMTllZS5iaW5kUG9wdXAocG9wdXBfZDU0MjQzM2FmYWIzNDJjNTlhNzVkZjUyNDk0M2Y1NmIpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKCiAgICAgICAgICAgIHZhciBtYXJrZXJfZTA0MjRjNDk1MjA1NDIwYjg4NzVlNDk3NjZjODExYzYgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFstMzcuMzU4NiwxNzkuMTQ2MV0sCiAgICAgICAgICAgICAgICB7CiAgICAgICAgICAgICAgICAgICAgaWNvbjogbmV3IEwuSWNvbi5EZWZhdWx0KCkKICAgICAgICAgICAgICAgICAgICB9CiAgICAgICAgICAgICAgICApCiAgICAgICAgICAgICAgICAuYWRkVG8obWFwX2EwNmY5Yzc4OGRmMDQzYzE5NGJlNTk1NmY5OWE2ZDA1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzkwNGM5NWU2ZGI1NjRlNTc4ZGQ4OTUyOTE2NzM5YjVjID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzQ0MTE0MWE0NjhkZDRhNzE4OWVhNmJlMzI5MmI2YTdiID0gJCgnPGRpdiBpZD0iaHRtbF80NDExNDFhNDY4ZGQ0YTcxODllYTZiZTMyOTJiNmE3YiIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+cGxhY2U6MTc1a20gTkUgb2YgR2lzYm9ybmUsIE5ldyBaZWFsYW5kIG1hZ25pdHVkZTo3PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF85MDRjOTVlNmRiNTY0ZTU3OGRkODk1MjkxNjczOWI1Yy5zZXRDb250ZW50KGh0bWxfNDQxMTQxYTQ2OGRkNGE3MTg5ZWE2YmUzMjkyYjZhN2IpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIG1hcmtlcl9lMDQyNGM0OTUyMDU0MjBiODg3NWU0OTc2NmM4MTFjNi5iaW5kUG9wdXAocG9wdXBfOTA0Yzk1ZTZkYjU2NGU1NzhkZDg5NTI5MTY3MzliNWMpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKCiAgICAgICAgICAgIHZhciBtYXJrZXJfODY2MGRiMjQzNTVlNDFhNTg4ZmMxMWIxNWYwZWViY2IgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFstMC4wNDU2LC0xNy44MjU1XSwKICAgICAgICAgICAgICAgIHsKICAgICAgICAgICAgICAgICAgICBpY29uOiBuZXcgTC5JY29uLkRlZmF1bHQoKQogICAgICAgICAgICAgICAgICAgIH0KICAgICAgICAgICAgICAgICkKICAgICAgICAgICAgICAgIC5hZGRUbyhtYXBfYTA2ZjljNzg4ZGYwNDNjMTk0YmU1OTU2Zjk5YTZkMDUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfYzU3YTY2MjA5OTkzNDlmNTg3ZjQzYjliMjU1Njc4MGQgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMDMxZTM1YmE4MTg2NGFjNjlmY2I4ZTUzMjNlNmY1N2EgPSAkKCc8ZGl2IGlkPSJodG1sXzAzMWUzNWJhODE4NjRhYzY5ZmNiOGU1MzIzZTZmNTdhIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5wbGFjZTpOb3J0aCBvZiBBc2NlbnNpb24gSXNsYW5kIG1hZ25pdHVkZTo3LjE8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2M1N2E2NjIwOTk5MzQ5ZjU4N2Y0M2I5YjI1NTY3ODBkLnNldENvbnRlbnQoaHRtbF8wMzFlMzViYTgxODY0YWM2OWZjYjhlNTMyM2U2ZjU3YSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgbWFya2VyXzg2NjBkYjI0MzU1ZTQxYTU4OGZjMTFiMTVmMGVlYmNiLmJpbmRQb3B1cChwb3B1cF9jNTdhNjYyMDk5OTM0OWY1ODdmNDNiOWIyNTU2NzgwZCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAoKICAgICAgICAgICAgdmFyIG1hcmtlcl84NzBmNGY1ZjdlMWM0MTJhOTg2OWFkMDJlNWVlN2JhZiA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWy01NS4yODUyLC0zMS44NzY2XSwKICAgICAgICAgICAgICAgIHsKICAgICAgICAgICAgICAgICAgICBpY29uOiBuZXcgTC5JY29uLkRlZmF1bHQoKQogICAgICAgICAgICAgICAgICAgIH0KICAgICAgICAgICAgICAgICkKICAgICAgICAgICAgICAgIC5hZGRUbyhtYXBfYTA2ZjljNzg4ZGYwNDNjMTk0YmU1OTU2Zjk5YTZkMDUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMzMxMTQyODJlOGVmNGM0OGEyZmY1ZjE0YTEyMzZiNzEgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNzQ2YWY3ZTIyOTQxNDNhYjg5YzIxZmZkZDE0MjY1NTIgPSAkKCc8ZGl2IGlkPSJodG1sXzc0NmFmN2UyMjk0MTQzYWI4OWMyMWZmZGQxNDI2NTUyIiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5wbGFjZTpTb3V0aCBHZW9yZ2lhIElzbGFuZCByZWdpb24gbWFnbml0dWRlOjcuNDwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfMzMxMTQyODJlOGVmNGM0OGEyZmY1ZjE0YTEyMzZiNzEuc2V0Q29udGVudChodG1sXzc0NmFmN2UyMjk0MTQzYWI4OWMyMWZmZGQxNDI2NTUyKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBtYXJrZXJfODcwZjRmNWY3ZTFjNDEyYTk4NjlhZDAyZTVlZTdiYWYuYmluZFBvcHVwKHBvcHVwXzMzMTE0MjgyZThlZjRjNDhhMmZmNWYxNGExMjM2YjcxKTsKCiAgICAgICAgICAgIAogICAgICAgIAogICAgCgogICAgICAgICAgICB2YXIgbWFya2VyXzhiNzE1ZDlhMGU0NDQzNDc5NjllZDVhYjY0MTk3Zjg1ID0gTC5tYXJrZXIoCiAgICAgICAgICAgICAgICBbLTIyLjQ3NjUsMTczLjExNjddLAogICAgICAgICAgICAgICAgewogICAgICAgICAgICAgICAgICAgIGljb246IG5ldyBMLkljb24uRGVmYXVsdCgpCiAgICAgICAgICAgICAgICAgICAgfQogICAgICAgICAgICAgICAgKQogICAgICAgICAgICAgICAgLmFkZFRvKG1hcF9hMDZmOWM3ODhkZjA0M2MxOTRiZTU5NTZmOTlhNmQwNSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF9hYTJmNzI3OWM0Yzg0MGViYjQ1YjYyM2JkODk5ZmJlZiA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF84YjA5YWE3ODFmMTg0MThlYjI1NWM0M2MyNTk5N2M5NyA9ICQoJzxkaXYgaWQ9Imh0bWxfOGIwOWFhNzgxZjE4NDE4ZWIyNTVjNDNjMjU5OTdjOTciIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPnBsYWNlOjExMGttIEUgb2YgSWxlIEh1bnRlciwgTmV3IENhbGVkb25pYSBtYWduaXR1ZGU6Ny4yPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9hYTJmNzI3OWM0Yzg0MGViYjQ1YjYyM2JkODk5ZmJlZi5zZXRDb250ZW50KGh0bWxfOGIwOWFhNzgxZjE4NDE4ZWIyNTVjNDNjMjU5OTdjOTcpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIG1hcmtlcl84YjcxNWQ5YTBlNDQ0MzQ3OTY5ZWQ1YWI2NDE5N2Y4NS5iaW5kUG9wdXAocG9wdXBfYWEyZjcyNzljNGM4NDBlYmI0NWI2MjNiZDg5OWZiZWYpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKCiAgICAgICAgICAgIHZhciBtYXJrZXJfYzkwMTU5ZjM2ZWJjNDhlZmI4YTI5MTc3NTI5OWJiNjYgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFsxOC41NDI5LDE0NS41MDczXSwKICAgICAgICAgICAgICAgIHsKICAgICAgICAgICAgICAgICAgICBpY29uOiBuZXcgTC5JY29uLkRlZmF1bHQoKQogICAgICAgICAgICAgICAgICAgIH0KICAgICAgICAgICAgICAgICkKICAgICAgICAgICAgICAgIC5hZGRUbyhtYXBfYTA2ZjljNzg4ZGYwNDNjMTk0YmU1OTU2Zjk5YTZkMDUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfMDEyMjlmMmI2Zjk0NGM0MGJkNDRhMmRlZDJhNWEyMWMgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfNzBmNDI5YWIyZjUxNDY2N2FjZjQ2NjkxMzE3ZjQwZjYgPSAkKCc8ZGl2IGlkPSJodG1sXzcwZjQyOWFiMmY1MTQ2NjdhY2Y0NjY5MTMxN2Y0MGY2IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5wbGFjZToyOWttIFNXIG9mIEFncmloYW4sIE5vcnRoZXJuIE1hcmlhbmEgSXNsYW5kcyBtYWduaXR1ZGU6Ny43PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8wMTIyOWYyYjZmOTQ0YzQwYmQ0NGEyZGVkMmE1YTIxYy5zZXRDb250ZW50KGh0bWxfNzBmNDI5YWIyZjUxNDY2N2FjZjQ2NjkxMzE3ZjQwZjYpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIG1hcmtlcl9jOTAxNTlmMzZlYmM0OGVmYjhhMjkxNzc1Mjk5YmI2Ni5iaW5kUG9wdXAocG9wdXBfMDEyMjlmMmI2Zjk0NGM0MGJkNDRhMmRlZDJhNWEyMWMpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKCiAgICAgICAgICAgIHZhciBtYXJrZXJfMzJjZjc2ZmY4N2NiNGM5OTkxZTRiODYyYmY1MDRiODIgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFstNTYuMjQwOSwtMjYuOTM1M10sCiAgICAgICAgICAgICAgICB7CiAgICAgICAgICAgICAgICAgICAgaWNvbjogbmV3IEwuSWNvbi5EZWZhdWx0KCkKICAgICAgICAgICAgICAgICAgICB9CiAgICAgICAgICAgICAgICApCiAgICAgICAgICAgICAgICAuYWRkVG8obWFwX2EwNmY5Yzc4OGRmMDQzYzE5NGJlNTk1NmY5OWE2ZDA1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzQwNDMzZDgxM2E5YTQ2MjM4NDVkMWU4NmJmZjExMmVjID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzUwZTQwNGU0Y2I4MjQwZjFiZWYwNTBjMTIyN2E2Njg3ID0gJCgnPGRpdiBpZD0iaHRtbF81MGU0MDRlNGNiODI0MGYxYmVmMDUwYzEyMjdhNjY4NyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+cGxhY2U6NTNrbSBOTkUgb2YgVmlzb2tvaSBJc2xhbmQsIFNvdXRoIEdlb3JnaWEgYW5kIHRoZSBTb3V0aCBTYW5kd2ljaCBJc2xhbmRzIG1hZ25pdHVkZTo3LjI8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzQwNDMzZDgxM2E5YTQ2MjM4NDVkMWU4NmJmZjExMmVjLnNldENvbnRlbnQoaHRtbF81MGU0MDRlNGNiODI0MGYxYmVmMDUwYzEyMjdhNjY4Nyk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgbWFya2VyXzMyY2Y3NmZmODdjYjRjOTk5MWU0Yjg2MmJmNTA0YjgyLmJpbmRQb3B1cChwb3B1cF80MDQzM2Q4MTNhOWE0NjIzODQ1ZDFlODZiZmYxMTJlYyk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAoKICAgICAgICAgICAgdmFyIG1hcmtlcl9kYTQyNGNmMmZiNDg0ZGE1OTBlYThiMzMxNzUxZTU3ZSA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWy0xNi4wNDI5LDE2Ny4zNzg2XSwKICAgICAgICAgICAgICAgIHsKICAgICAgICAgICAgICAgICAgICBpY29uOiBuZXcgTC5JY29uLkRlZmF1bHQoKQogICAgICAgICAgICAgICAgICAgIH0KICAgICAgICAgICAgICAgICkKICAgICAgICAgICAgICAgIC5hZGRUbyhtYXBfYTA2ZjljNzg4ZGYwNDNjMTk0YmU1OTU2Zjk5YTZkMDUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfM2I0MDk5NGIyZDJhNDE3Mzg0OGQ5YjBiY2FlZWU5MzggPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfMGY3ZTU4MmRkZThkNGU0MThjYmQxZGI2YjM1Y2EwZjkgPSAkKCc8ZGl2IGlkPSJodG1sXzBmN2U1ODJkZGU4ZDRlNDE4Y2JkMWRiNmIzNWNhMGY5IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5wbGFjZToya20gTiBvZiBOb3JzdXAsIFZhbnVhdHUgbWFnbml0dWRlOjc8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzNiNDA5OTRiMmQyYTQxNzM4NDhkOWIwYmNhZWVlOTM4LnNldENvbnRlbnQoaHRtbF8wZjdlNTgyZGRlOGQ0ZTQxOGNiZDFkYjZiMzVjYTBmOSk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgbWFya2VyX2RhNDI0Y2YyZmI0ODRkYTU5MGVhOGIzMzE3NTFlNTdlLmJpbmRQb3B1cChwb3B1cF8zYjQwOTk0YjJkMmE0MTczODQ4ZDliMGJjYWVlZTkzOCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAoKICAgICAgICAgICAgdmFyIG1hcmtlcl8zOThkN2M3YjgxZDg0NGNhYmZmYjE4ODNlM2I5NjkxYiA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzAuMzgxOSwtNzkuOTIxOF0sCiAgICAgICAgICAgICAgICB7CiAgICAgICAgICAgICAgICAgICAgaWNvbjogbmV3IEwuSWNvbi5EZWZhdWx0KCkKICAgICAgICAgICAgICAgICAgICB9CiAgICAgICAgICAgICAgICApCiAgICAgICAgICAgICAgICAuYWRkVG8obWFwX2EwNmY5Yzc4OGRmMDQzYzE5NGJlNTk1NmY5OWE2ZDA1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwX2Q1MGY3YzhkZWJiODQ2ODNiMTY0ZTQ5ZmMxNGQ3NGY4ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzE3ZDhiM2UxMTI1ZTQyNjlhYzBiNjliOGQwMTE1NzkzID0gJCgnPGRpdiBpZD0iaHRtbF8xN2Q4YjNlMTEyNWU0MjY5YWMwYjY5YjhkMDExNTc5MyIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+cGxhY2U6MjdrbSBTU0Ugb2YgTXVpc25lLCBFY3VhZG9yIG1hZ25pdHVkZTo3Ljg8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwX2Q1MGY3YzhkZWJiODQ2ODNiMTY0ZTQ5ZmMxNGQ3NGY4LnNldENvbnRlbnQoaHRtbF8xN2Q4YjNlMTEyNWU0MjY5YWMwYjY5YjhkMDExNTc5Myk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgbWFya2VyXzM5OGQ3YzdiODFkODQ0Y2FiZmZiMTg4M2UzYjk2OTFiLmJpbmRQb3B1cChwb3B1cF9kNTBmN2M4ZGViYjg0NjgzYjE2NGU0OWZjMTRkNzRmOCk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAoKICAgICAgICAgICAgdmFyIG1hcmtlcl81MmQ4NTEwY2JjYWQ0ZmQ2OTA0ZmE5ODhkZGJiNjRhYiA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWzMyLjc5MDYsMTMwLjc1NDNdLAogICAgICAgICAgICAgICAgewogICAgICAgICAgICAgICAgICAgIGljb246IG5ldyBMLkljb24uRGVmYXVsdCgpCiAgICAgICAgICAgICAgICAgICAgfQogICAgICAgICAgICAgICAgKQogICAgICAgICAgICAgICAgLmFkZFRvKG1hcF9hMDZmOWM3ODhkZjA0M2MxOTRiZTU5NTZmOTlhNmQwNSk7CiAgICAgICAgICAgIAogICAgCiAgICAgICAgICAgIHZhciBwb3B1cF8wNjg1NDJmYWE2ZWE0NTAwOTc0ZWYzYzFkNWVmZjNhNyA9IEwucG9wdXAoe21heFdpZHRoOiAnMzAwJ30pOwoKICAgICAgICAgICAgCiAgICAgICAgICAgICAgICB2YXIgaHRtbF9mZDE0YTk5NmM4NjI0MjIwOTAxMWY2Mzg2NzJiYmM2NyA9ICQoJzxkaXYgaWQ9Imh0bWxfZmQxNGE5OTZjODYyNDIyMDkwMTFmNjM4NjcyYmJjNjciIHN0eWxlPSJ3aWR0aDogMTAwLjAlOyBoZWlnaHQ6IDEwMC4wJTsiPnBsYWNlOjFrbSBFIG9mIEt1bWFtb3RvLXNoaSwgSmFwYW4gbWFnbml0dWRlOjc8L2Rpdj4nKVswXTsKICAgICAgICAgICAgICAgIHBvcHVwXzA2ODU0MmZhYTZlYTQ1MDA5NzRlZjNjMWQ1ZWZmM2E3LnNldENvbnRlbnQoaHRtbF9mZDE0YTk5NmM4NjI0MjIwOTAxMWY2Mzg2NzJiYmM2Nyk7CiAgICAgICAgICAgIAoKICAgICAgICAgICAgbWFya2VyXzUyZDg1MTBjYmNhZDRmZDY5MDRmYTk4OGRkYmI2NGFiLmJpbmRQb3B1cChwb3B1cF8wNjg1NDJmYWE2ZWE0NTAwOTc0ZWYzYzFkNWVmZjNhNyk7CgogICAgICAgICAgICAKICAgICAgICAKICAgIAoKICAgICAgICAgICAgdmFyIG1hcmtlcl8yYzUzMjMzZGIyYTg0MTQ0YTliNmVkZGFkNTBlNDA3ZiA9IEwubWFya2VyKAogICAgICAgICAgICAgICAgWy00Ljk1MjEsOTQuMzI5OV0sCiAgICAgICAgICAgICAgICB7CiAgICAgICAgICAgICAgICAgICAgaWNvbjogbmV3IEwuSWNvbi5EZWZhdWx0KCkKICAgICAgICAgICAgICAgICAgICB9CiAgICAgICAgICAgICAgICApCiAgICAgICAgICAgICAgICAuYWRkVG8obWFwX2EwNmY5Yzc4OGRmMDQzYzE5NGJlNTk1NmY5OWE2ZDA1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzI2NmJmMGJjYmU0MjRlZjU4ZTcyYWY5ZThhZjU3Mzc2ID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sX2Q4YmE1N2UzNDI3ZTQxZTk5ZmU5NGJhNGUzNTE3NTk5ID0gJCgnPGRpdiBpZD0iaHRtbF9kOGJhNTdlMzQyN2U0MWU5OWZlOTRiYTRlMzUxNzU5OSIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+cGxhY2U6U291dGh3ZXN0IG9mIFN1bWF0cmEsIEluZG9uZXNpYSBtYWduaXR1ZGU6Ny44PC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF8yNjZiZjBiY2JlNDI0ZWY1OGU3MmFmOWU4YWY1NzM3Ni5zZXRDb250ZW50KGh0bWxfZDhiYTU3ZTM0MjdlNDFlOTlmZTk0YmE0ZTM1MTc1OTkpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIG1hcmtlcl8yYzUzMjMzZGIyYTg0MTQ0YTliNmVkZGFkNTBlNDA3Zi5iaW5kUG9wdXAocG9wdXBfMjY2YmYwYmNiZTQyNGVmNThlNzJhZjllOGFmNTczNzYpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKCiAgICAgICAgICAgIHZhciBtYXJrZXJfYjQzZjI4NjIzZGU3NDc4ZDkyYTM4NDJiMmI3NDY4OTMgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs1My45Nzc2LDE1OC41NDYzXSwKICAgICAgICAgICAgICAgIHsKICAgICAgICAgICAgICAgICAgICBpY29uOiBuZXcgTC5JY29uLkRlZmF1bHQoKQogICAgICAgICAgICAgICAgICAgIH0KICAgICAgICAgICAgICAgICkKICAgICAgICAgICAgICAgIC5hZGRUbyhtYXBfYTA2ZjljNzg4ZGYwNDNjMTk0YmU1OTU2Zjk5YTZkMDUpOwogICAgICAgICAgICAKICAgIAogICAgICAgICAgICB2YXIgcG9wdXBfZmU5ZTMyOWVjN2I0NDQ5YjllYmE5MGQ0ODZlOWFmZWQgPSBMLnBvcHVwKHttYXhXaWR0aDogJzMwMCd9KTsKCiAgICAgICAgICAgIAogICAgICAgICAgICAgICAgdmFyIGh0bWxfYzI5NGJkNjhkODg0NDY5ZTk1NzFlZDEyMGQwZmMzOTcgPSAkKCc8ZGl2IGlkPSJodG1sX2MyOTRiZDY4ZDg4NDQ2OWU5NTcxZWQxMjBkMGZjMzk3IiBzdHlsZT0id2lkdGg6IDEwMC4wJTsgaGVpZ2h0OiAxMDAuMCU7Ij5wbGFjZTo4OGttIE4gb2YgWWVsaXpvdm8sIFJ1c3NpYSBtYWduaXR1ZGU6Ny4yPC9kaXY+JylbMF07CiAgICAgICAgICAgICAgICBwb3B1cF9mZTllMzI5ZWM3YjQ0NDliOWViYTkwZDQ4NmU5YWZlZC5zZXRDb250ZW50KGh0bWxfYzI5NGJkNjhkODg0NDY5ZTk1NzFlZDEyMGQwZmMzOTcpOwogICAgICAgICAgICAKCiAgICAgICAgICAgIG1hcmtlcl9iNDNmMjg2MjNkZTc0NzhkOTJhMzg0MmIyYjc0Njg5My5iaW5kUG9wdXAocG9wdXBfZmU5ZTMyOWVjN2I0NDQ5YjllYmE5MGQ0ODZlOWFmZWQpOwoKICAgICAgICAgICAgCiAgICAgICAgCiAgICAKCiAgICAgICAgICAgIHZhciBtYXJrZXJfMjIzMjcwMTliZTk4NDFmODhmZmFmZmU2Mzk2OWY2NDAgPSBMLm1hcmtlcigKICAgICAgICAgICAgICAgIFs1OS42MzYzLC0xNTMuNDA1MV0sCiAgICAgICAgICAgICAgICB7CiAgICAgICAgICAgICAgICAgICAgaWNvbjogbmV3IEwuSWNvbi5EZWZhdWx0KCkKICAgICAgICAgICAgICAgICAgICB9CiAgICAgICAgICAgICAgICApCiAgICAgICAgICAgICAgICAuYWRkVG8obWFwX2EwNmY5Yzc4OGRmMDQzYzE5NGJlNTk1NmY5OWE2ZDA1KTsKICAgICAgICAgICAgCiAgICAKICAgICAgICAgICAgdmFyIHBvcHVwXzZlZDE5NjdlYTg3ODRkNTNiOTk3NDZmNjhjM2Q3MGIxID0gTC5wb3B1cCh7bWF4V2lkdGg6ICczMDAnfSk7CgogICAgICAgICAgICAKICAgICAgICAgICAgICAgIHZhciBodG1sXzJmMWQyZDM5MmE1NzRlODZhMjZiMDhmNzljYWJhNTgwID0gJCgnPGRpdiBpZD0iaHRtbF8yZjFkMmQzOTJhNTc0ZTg2YTI2YjA4Zjc5Y2FiYTU4MCIgc3R5bGU9IndpZHRoOiAxMDAuMCU7IGhlaWdodDogMTAwLjAlOyI+cGxhY2U6ODZrbSBFIG9mIE9sZCBJbGlhbW5hLCBBbGFza2EgbWFnbml0dWRlOjcuMTwvZGl2PicpWzBdOwogICAgICAgICAgICAgICAgcG9wdXBfNmVkMTk2N2VhODc4NGQ1M2I5OTc0NmY2OGMzZDcwYjEuc2V0Q29udGVudChodG1sXzJmMWQyZDM5MmE1NzRlODZhMjZiMDhmNzljYWJhNTgwKTsKICAgICAgICAgICAgCgogICAgICAgICAgICBtYXJrZXJfMjIzMjcwMTliZTk4NDFmODhmZmFmZmU2Mzk2OWY2NDAuYmluZFBvcHVwKHBvcHVwXzZlZDE5NjdlYTg3ODRkNTNiOTk3NDZmNjhjM2Q3MGIxKTsKCiAgICAgICAgICAgIAogICAgICAgIAo8L3NjcmlwdD4=" style="position:absolute;width:100%;height:100%;left:0;top:0;border:none !important;" allowfullscreen webkitallowfullscreen mozallowfullscreen></iframe></div></div>



### When?

Jupyter Notebooks can be used in a variety of contexts, only a few of which are mentioned below:

* documenting homework,
* documenting an algorithm or research methodology,
* writing a paper that is about code or a dataset,
* developing and documenting a research idea that explores a theoretical result backed by an implementation (code),
* exploring and documenting a dataset or an algorithm on a specific dataset,
* testing code,
* playing with code,
* and many other contexts.


### Resources
The best place to begin learning how to use Jupyter is to go directly to 

* the [Jupyter.org](https://jupyter.org) site,
* but for inspiration see the [gallery of Jupyter examples](https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks)
* and some for [Earth Sciences](https://github.com/jupyter/jupyter/wiki/A-gallery-of-interesting-Jupyter-Notebooks#earth-science-and-geo-spatial-data-1) notebooks examples,
* and another [general gallery](http://nb.bianp.net/sort/views/), 
* and many, many more you may find and explore on your own ...
