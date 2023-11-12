# Mutation_Testing
An application used to demonstrate mutation testing techniques. This will use the python library [Mutatest](https://mutatest.readthedocs.io/en/latest/install.html) to perform mutation generation.

## Defining Mutation Operators
- Mutatest does most of this testing, but it is important to note that certain tests can be excluded.
- The mutation operators include examples like (- -> +) and (/ -> %) in this case. This simply means thats subtraction will be changed to addititon for example. 
- More mutations include swapping true to false and false to true, which should introduce a mutation.
- Mutatest also changes the comparison opperators. Examples include changing != to == which should also result in a mutation.
- Mutatest even provides mutation for indexs and slicing, but they will not be utalized in this application.

## Description of Applied Mutations and Impacts of the Mutations
- The implementation of this mutation file is done by Mutatest. Mutatest actually modifies the pycache file to avoid editing the source code directly. This method ensures that the mutations are not directly commited to any type of version control.
- The following are examples of how the mutation testing is done on the source code. These examples are taken from the Mutatest documentation.
- ![Example 1](mutation_example1.png)
- ![Example 2](mutation_example2.png)
- This following example shows how it is applied to the Test_Poly source code.
- ![Example 3](mutation_example3.png)
- ![Exmaple 4](mutation_example4.png)
- All of the previous examples should introduce mutations. However if the code is well written, then the mutations should be killed as soon as they appear.

## Summary of Mutant Survival and Killing

#### Console Output

(venv) @justyden ➜ /workspaces/Mutation_Testing (main) $ mutatest -s src/
2023-11-12 20:11:35,784: Running clean trial
=================================================================== test session starts ====================================================================
platform linux -- Python 3.10.8, pytest-7.4.3, pluggy-1.3.0
rootdir: /workspaces/Mutation_Testing
collected 8 items                                                                                                                                          

src/test/test_poly.py ........                                                                                                                       [100%]

==================================================================== 8 passed in 0.02s =====================================================================
2023-11-12 20:11:35,989: 55 mutation targets found in src/Polynomial.py AST.
2023-11-12 20:11:35,989: Setting random.seed to: None
2023-11-12 20:11:35,990: Coverage file does not exist, proceeding to sample from all targets.
2023-11-12 20:11:35,990: Total sample space size: 55
2023-11-12 20:11:35,990: Selecting 10 locations from 55 potentials.
2023-11-12 20:11:35,990: Starting individual mutation trials!
2023-11-12 20:11:35,990: Running serial (single processor) dispatch mode.
2023-11-12 20:11:35,990: Current target location: Polynomial.py, LocIndex(ast_class='If', lineno=22, col_offset=16, op_type='If_Statement', end_lineno=25, end_col_offset=70)
2023-11-12 20:11:36,214: Result: Detected at src/Polynomial.py: (22, 16)
2023-11-12 20:11:36,436: Result: Detected at src/Polynomial.py: (22, 16)
2023-11-12 20:11:36,436: Current target location: Polynomial.py, LocIndex(ast_class='BinOp', lineno=73, col_offset=16, op_type=<class 'ast.Mult'>, end_lineno=73, end_col_offset=23)
2023-11-12 20:11:36,664: Result: Survived at src/Polynomial.py: (73, 16)
2023-11-12 20:11:36,664: Break on survival: stopping further mutations at location.
2023-11-12 20:11:36,664: Current target location: Polynomial.py, LocIndex(ast_class='Compare', lineno=18, col_offset=15, op_type=<class 'ast.Eq'>, end_lineno=18, end_col_offset=24)
2023-11-12 20:11:36,887: Result: Detected at src/Polynomial.py: (18, 15)
2023-11-12 20:11:37,113: Result: Detected at src/Polynomial.py: (18, 15)
2023-11-12 20:11:37,366: Result: Detected at src/Polynomial.py: (18, 15)
2023-11-12 20:11:37,589: Result: Detected at src/Polynomial.py: (18, 15)
2023-11-12 20:11:37,814: Result: Detected at src/Polynomial.py: (18, 15)
2023-11-12 20:11:37,815: Current target location: Polynomial.py, LocIndex(ast_class='AugAssign', lineno=66, col_offset=12, op_type='AugAssign_Add', end_lineno=66, end_col_offset=68)
2023-11-12 20:11:38,047: Result: Detected at src/Polynomial.py: (66, 12)
2023-11-12 20:11:38,249: Result: Survived at src/Polynomial.py: (66, 12)
2023-11-12 20:11:38,249: Break on survival: stopping further mutations at location.
2023-11-12 20:11:38,249: Current target location: Polynomial.py, LocIndex(ast_class='BinOp', lineno=25, col_offset=39, op_type=<class 'ast.Sub'>, end_lineno=25, end_col_offset=69)
2023-11-12 20:11:38,482: Result: Detected at src/Polynomial.py: (25, 39)
2023-11-12 20:11:38,726: Result: Detected at src/Polynomial.py: (25, 39)
2023-11-12 20:11:38,954: Result: Detected at src/Polynomial.py: (25, 39)
2023-11-12 20:11:39,180: Result: Detected at src/Polynomial.py: (25, 39)
2023-11-12 20:11:39,403: Result: Detected at src/Polynomial.py: (25, 39)
2023-11-12 20:11:39,659: Result: Detected at src/Polynomial.py: (25, 39)
2023-11-12 20:11:39,659: Current target location: Polynomial.py, LocIndex(ast_class='BinOp', lineno=44, col_offset=22, op_type=<class 'ast.Add'>, end_lineno=44, end_col_offset=85)
2023-11-12 20:11:40,021: Result: Error at src/Polynomial.py: (44, 22)
2023-11-12 20:11:40,021: Break on error: stopping further mutations at location.
2023-11-12 20:11:40,021: Current target location: Polynomial.py, LocIndex(ast_class='BinOp', lineno=34, col_offset=22, op_type=<class 'ast.Add'>, end_lineno=34, end_col_offset=85)
2023-11-12 20:11:40,378: Result: Error at src/Polynomial.py: (34, 22)
2023-11-12 20:11:40,378: Break on error: stopping further mutations at location.
2023-11-12 20:11:40,378: Current target location: Polynomial.py, LocIndex(ast_class='Compare', lineno=13, col_offset=11, op_type=<class 'ast.Eq'>, end_lineno=13, end_col_offset=38)
2023-11-12 20:11:40,609: Result: Detected at src/Polynomial.py: (13, 11)
2023-11-12 20:11:40,846: Result: Detected at src/Polynomial.py: (13, 11)
2023-11-12 20:11:41,073: Result: Survived at src/Polynomial.py: (13, 11)
2023-11-12 20:11:41,073: Break on survival: stopping further mutations at location.
2023-11-12 20:11:41,074: Current target location: Polynomial.py, LocIndex(ast_class='Compare', lineno=91, col_offset=19, op_type=<class 'ast.Lt'>, end_lineno=91, end_col_offset=50)
2023-11-12 20:11:41,282: Result: Survived at src/Polynomial.py: (91, 19)
2023-11-12 20:11:41,282: Break on survival: stopping further mutations at location.
2023-11-12 20:11:41,282: Current target location: Polynomial.py, LocIndex(ast_class='BinOp', lineno=89, col_offset=20, op_type=<class 'ast.Div'>, end_lineno=89, end_col_offset=31)
2023-11-12 20:11:41,641: Result: Error at src/Polynomial.py: (89, 20)
2023-11-12 20:11:41,641: Break on error: stopping further mutations at location.
2023-11-12 20:11:41,642: Running clean trial
=================================================================== test session starts ====================================================================
platform linux -- Python 3.10.8, pytest-7.4.3, pluggy-1.3.0
rootdir: /workspaces/Mutation_Testing
collected 8 items                                                                                                                                          

src/test/test_poly.py ........                                                                                                                       [100%]

==================================================================== 8 passed in 0.02s =====================================================================
2023-11-12 20:11:41,858: CLI Report:

##### Mutatest diagnostic summary
===========================
 - Source location: /workspaces/Mutation_Testing/src
 - Test commands: ['pytest']
 - Mode: s
 - Excluded files: []
 - N locations input: 10
 - Random seed: None

##### Random sample details
---------------------
 - Total locations mutated: 10
 - Total locations identified: 55
 - Location sample coverage: 18.18 %


##### Running time details
--------------------
 - Clean trial 1 run time: 0:00:00.201581
 - Clean trial 2 run time: 0:00:00.215790
 - Mutation trials total run time: 0:00:05.654891

2023-11-12 20:11:41,859: Trial Summary Report:

##### Overall mutation trial summary
==============================
 - DETECTED: 16
 - SURVIVED: 4
 - ERROR: 3
 - TOTAL RUNS: 23
 - RUN DATETIME: 2023-11-12 20:11:41.858471

2023-11-12 20:11:41,859: Detected mutations:

##### DETECTED
--------
 - src/Polynomial.py: (l: 13, c: 11) - mutation from <class 'ast.Eq'> to <class 'ast.GtE'>
 - src/Polynomial.py: (l: 13, c: 11) - mutation from <class 'ast.Eq'> to <class 'ast.Gt'>
 - src/Polynomial.py: (l: 18, c: 15) - mutation from <class 'ast.Eq'> to <class 'ast.LtE'>
 - src/Polynomial.py: (l: 18, c: 15) - mutation from <class 'ast.Eq'> to <class 'ast.NotEq'>
 - src/Polynomial.py: (l: 18, c: 15) - mutation from <class 'ast.Eq'> to <class 'ast.Lt'>
 - src/Polynomial.py: (l: 18, c: 15) - mutation from <class 'ast.Eq'> to <class 'ast.GtE'>
 - src/Polynomial.py: (l: 18, c: 15) - mutation from <class 'ast.Eq'> to <class 'ast.Gt'>
 - src/Polynomial.py: (l: 22, c: 16) - mutation from If_Statement to If_False
 - src/Polynomial.py: (l: 22, c: 16) - mutation from If_Statement to If_True
 - src/Polynomial.py: (l: 25, c: 39) - mutation from <class 'ast.Sub'> to <class 'ast.Mod'>
 - src/Polynomial.py: (l: 25, c: 39) - mutation from <class 'ast.Sub'> to <class 'ast.Pow'>
 - src/Polynomial.py: (l: 25, c: 39) - mutation from <class 'ast.Sub'> to <class 'ast.Mult'>
 - src/Polynomial.py: (l: 25, c: 39) - mutation from <class 'ast.Sub'> to <class 'ast.FloorDiv'>
 - src/Polynomial.py: (l: 25, c: 39) - mutation from <class 'ast.Sub'> to <class 'ast.Div'>
 - src/Polynomial.py: (l: 25, c: 39) - mutation from <class 'ast.Sub'> to <class 'ast.Add'>
 - src/Polynomial.py: (l: 66, c: 12) - mutation from AugAssign_Add to AugAssign_Mult

2023-11-12 20:11:41,859: Timedout mutations:

2023-11-12 20:11:41,859: Surviving mutations:

##### SURVIVED
--------
 - src/Polynomial.py: (l: 13, c: 11) - mutation from <class 'ast.Eq'> to <class 'ast.Lt'>
 - src/Polynomial.py: (l: 66, c: 12) - mutation from AugAssign_Add to AugAssign_Sub
 - src/Polynomial.py: (l: 73, c: 16) - mutation from <class 'ast.Mult'> to <class 'ast.Div'>
 - src/Polynomial.py: (l: 91, c: 19) - mutation from <class 'ast.Lt'> to <class 'ast.LtE'>

## Analysis of the Test Suite Effectiveness
- It can be seen that there were quite a few mutations that ended up surving from the coverage report.
- The mutations that survived
- ![Survived Mutations](mutation_example5.png)
- There are a few harmless mutations that survived, Including mutations from < and <= in this case.
- There were also a few harmful ones that survived. Some examples were subtraction and addition,
as well as < and = , which could result in some serious erros.

### Recommendations for Improving the Test Suite
Improving the test suite also comes when the added draw back of adding more computation time. This is because mutations are created
exponentially, and for this reason, it is not always the best case to through this into the building process. For small applications this is completely. Various ways of improving this application involve directly modifying mutatest input parameters and creating custom mutations. For the most part, mutatest handles almost all mutations, but there are a few specific scenarios where new mutations parameters should be created. This is more prominent in large scale applications.

## Conclusion
Mutations are a very powerful software engineering design practice and can help detect problems in code earlier. They were by introducing scenarios in the code that should never work. If they do end up working, then the mutations survives, in which it is up to the developer to find the bug and fix it.