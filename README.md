## About 


* Exercise implementing Constraint Satisfaction Problems (CSP) by implementing the N-Queens problem using symbolic constraints in a Jupyter notebook, and solving it using the Backtracking Search algorithm from AIMA.

To launch the notebook, run the following command from a terminal with anaconda3 installed and on the application path:

* Guide on Jupiter Notebook https://www.datacamp.com/community/tutorials/tutorial-jupyter-notebook#gs.WPbJuKE

## Setup

* Install Jupyter Notebook App with Miniconda http://jupyter.readthedocs.io/en/latest/install.html
    ```
    pip3 install --upgrade pip setuptools
    pip3 install jupyter
    pip3 install matplotlib util sympy
    ```

* Launch Jupyter Notebook App `jupyter notebook AIND-Constraint_Satisfaction.ipynb`

* Run code:
    * Click any section containing a code snippet and go to menu: Cells > Run All,
    then view the outputs shown below the code snippets

## Solution - Sympy

* http://localhost:8888/notebooks/Sympy_Intro.ipynb

# Warmup: Add to top of code snippet

`pip3 install sympy`

# SymPy Exercises

* Question 1
	* Solution 
		```
		A = symbols("A:A0, A:A1, A:A2")
		```

* Question 2
	* Solution
		```
		from operator import xor
		x, y = symbols("x y")
		xor_relation = xor(x, y)
		# alternative:
		# xor_relation = x ^ y
		E = xor_relation
		```

* Question 3
	* Solution
		```
		a, b, c = symbols(['a', 'b', 'c'])
		maxAbsDiff = constraint("MaxAbsDiff", abs(a - b) < c)

		A = symbols("A:A0, A:A1, A:A2")
		maxAbsDiff_copy = maxAbsDiff.subs({a: A[0], b: A[1], c: A[2]})
		```

* Question 4
	* Attempt (WRONG)
		https://discussions.udacity.com/t/sympy-intro-lab-question-4-help/229192/8

## Solution 

* diffDiag
	* Discussion https://discussions.udacity.com/t/diffdiag-using-symbol/229264/8