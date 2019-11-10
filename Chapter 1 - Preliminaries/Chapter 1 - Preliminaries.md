**## Chapter 1 - Preliminaries**

* * *


**What Kinds of Data?**

When I say "data", what am I referring to exactly? The primary focus is on **structured data**

* It’s a vague term that encompasses many different forms

* These forms are:

* **Tabular** or spreadsheet-like data in which each column may be a different type (string, numeric, date, etc.). This includes most kinds of data commonly stored in relational databases.

* **Multidimensional arrays** or matrices.

* Multiple tables of data interrelated by key columns

* Evenly or unevenly spaced time series

* This is by no means a complete list

**Why Python for Data Analysis?**

* Scripting languages: they can be used to quickly write small programs, or scripts to automate other tasks.

* Don’t be misled, just because it’s called a "scripting language", it does not mean that it cannot be used for building serious software.

* Python’s improved support of libraries like R, MATLAB, and others.

* Combined with Python’s overall strength for general-purpose software engineering, it is an excellent option as a primary language for building data applications.

**Python as Glue**

* Python’s success in scientific computing is the ease of integrating C, C++, and FORTRAN code.

* They share similar set of legacy FORTRAN and C libraries for doing linear algebra, optimization, integration, fast Fourier transforms, and other such algorithms.

**Solving the "Two-Language" Problem**

* It is common to research, prototype, and test new ideas using a more specialized computing language like SAS or R.

* Later port those ideas to be part of a larger production system written in Java, C#, or C++, for example.

* Python is a suitable language not only for research and prototyping but also for building the production systems.

* "Why maintain two development environments when one will suffice?"

* KISS principle - "Keep it simple, stupid"

**Why Not Python?**

* There are a number of uses which Python may be less suitable.

* Python is an interpreted programming language

* It will run substantially slower than code written in a compiled language (i.e Java or C++).

* Python can be challenging language for building highly concurrent, multithreaded applications, particularly applications with many CPU-bound threads.

    * Global Interpreter Lock (GIL), a mechanism that prevents the interpreter from executing more than one Python instruction at a time.

**Essential Python Libraries**

* **NumPy**

* Short form "Numerical Python"

* Cornerstone of numerical computing in Python.

* Provides data structures, algorithms and library glue needed for most scientific applications involving numerical data in Python.

* It contains, among other things:

    * A fast and efficient multidimensional array object *ndarray*

    * Functions for performing element-wise computations with arrays or mathematical operations between arrays.

    * Tools for reading and writing array-based datasets to disk

    * Linear algebra operations, Fourier transform, and random number generation

    * A mature C API to enable Python extensions and native C or C++ code to access NumPy’s data structures and computational facilities.

* NumPy are more efficient for storing and manipulating data than the other built-in Python data structures.

* Libraries written in a lower-level language, such as C or Fortran, can operate on the data stored in a NumPy array without copying data into some other memory representation.

* Thus, many numerical computing tools for Python either assume NumPy arrays as primary data structure.

* **Pandas**

* Provides high-level data structures and functions designed to make working with structured or tabular data fast, easy, and expressive.

* The primary objects in Pandas are *DataFrame*, a tabular, column-oriented data structure with both row and column labels.

* Another primary object is *Series*, a one-dimensional labeled array object.

* Pandas blends the high-performance, array-computing ideas of NumPy with the flexible data manipulation capabilities of spreadsheets and relational databases (i.e SQL).

* Sophisticated indexing functionality to make it easy to reshape, slice and dice, perform aggregations, and select subsets of data.

* Pandas helps with data manipulation, preparation, and cleaning.

* Pandas’ name itself is derived from *panel data*, an econometrics term for multidimensional structured datasets, and a play on the phrase *Python data analysis* itself.

**Matplotlib**

* Matplotlib is the most popular Python library for producing plots and other two-dimensional data visualizations.

* Designed for creating plots suitable for publication

**IPython** ** and Jupyter**

* IPython was created to make a better interactive Python interpreter (by Fernando Perez)

* One of the most important tools in the modern Python data stack

* IPython is designed to maximize your productivity in both interactive computing and software development.

* Encourages a *execute-explore* workflow instead of the typical *edit-compile-run* workflow of many other programming languages.

* Since much of data analysis coding involves exploration, trial and error, and iteration, IPython can help you get the job done faster

* IPython team announced Jupyter project in 2014.

* Jupyter is a broader initiative to design language-agnostic interactive computing tools.

* IPython can now be used as a *kernel *(a programming language mode) for using Python with Jupyter

* IPython provides a productive environment for interactive and exploratory computing.

* You can also use the IPython system through Jupyter Notebook, an interactive web-based code "notebook" offering support for dozens of programming languages.

* The IPython and Jupyter notebooks are especially useful for data exploration and visualization

**SciPy**

* SciPy is a collection of packages addressing a number of different standard problem domains in scientific computing.

* Here are a sampling of the packages included:

    * scipy.integrate

        * Numerical integration routines and differential equation solvers

    * scipy.linalg

        * Linear algebra routines and matrix decompositions extending beyond those provided in numpy.linalg

    * scipy.optimize

        * Function optimizers (minimizers) and root finding algorithms

    * scipy.signal

        * Signal processing tools

    * scipy.sparce

        * Sparse matrices and sparse linear system solvers

    * scipy.special

        * Wrapper around SPECFUN, a Fortran library implementing many common mathematical functions, such as the *gamma* function

    * scipy.stats

        * Standard continuous and discrete probability distributions (density functions, samplers, continuous distribution functions), various statistical tests, and more descriptive statistics. 

* Together NumPy and SciPy form a reasonably complete and mature computational foundation for many traditional scientific computing applications

**Scikit-learn**

* Scikit-learn has become the premier general-purpose machine learning toolkit for Python programmers.

* It includes submodels:

    * Classification: SVM, nearest neighbors, random forest, logistic regression, etc.

    * Regression: Lasso, ridge regression, etc.

    * Dimensionality reduction: PCA, feature selection, matrix factorization, etc.

    * Model Selection: Grid search, cross-validation, metrics.

    * Preprocessing: Feature extraction, normalization

* Along with pandas, statsmodels, and IPython, scikit-learn has been critical for enabling Python to be a productive data science programming language.

**Statsmodels**

* statsmodel is a statistical analysis package that was seeded by work from Stanford University statistics professor Jonathan Taylor.

* He implemented a number of regression analysis models popular in the R programming language.

* Compared with scikit-learn, statsmodel contain algorithms for classical (primarily frequentist) statistics and econometrics.

* These includes such submodels as:

    * Regression models: Linear regression, generalized linear models, robust linear models, linear mixed effects models, etc.

    * Analysis of variance (ANOVA)

    * Time series analysis: AR, ARMA, ARIMA, VAR, and other models

    * Nonparametric methods: Kernel density estimation, kernel regression

    * Visualization of statistical model results

* statsmodel is more focused on statistical inference, providing uncertainty estimates an p-values for parameters. Scikit-learn, by contrast, is more prediction-focused.

**Navigating This Book**

* Tasks required generally fall into a number of different broad groups:

    * Interacting with the outside world	

        * Reading and writing a variety of file formats and data stores

    * Preparation

        * Cleaning, munging, combining, normalizing, reshaping, slicing and dicing, and transforming data for analysis

    * Transformation

        * Applying mathematical and statistical operations to groups of datasets to derive new datasets (e.g aggregating a large table by group variables)

    * Modeling and computation

        * Connecting your data to statistical models, machine learning algorithms, or other computational tools.

    * Presentation

        * Creating interactive or static graphical visualizations or textual summaries

**Jargon**

* *Munge/munging/wrangling*

    * *Describes the overall process of manipulating unstructured *and/or messy data into a structured or clean form. The word has snuck its way into the jargon of many modern-day data hackers. "Munge" rhymes with “grunge”.

* *Pseudocode*

    * A description of an algorithm or process that takes a code-like form while likely not being actual valid source code.

* *Syntactic sugar*

    * Programming syntax that does not add new features, but makes something more convenient or easier to type.

