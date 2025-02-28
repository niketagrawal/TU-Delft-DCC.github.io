---
# Insert this YAML header (including the opening and closing ---) at the beginning of the document and fill it out accordingly

# We use this key to indicate the last reviewed date [manual entry, use YYYY-MM-DD]
# Uncomment and populate the next line accordingly
date: 2025-02-28

# We use this key to indicate the last modified date [automatic entry]
date-modified: last-modified

# Do not modify
lang: en
language: 
  title-block-published: "Last reviewed"
  title-block-modified: "Last modified"

# Title of the document [manual entry]
# Uncomment and populate the next line accordingly
title: Writing integration tests in Python

# Brief overview of the document (will be used in listings) [manual entry]
# Uncomment and populate the next line and uncomment "hide-description: true".
#description: Short description of the document
#hide-description: true

# Authors of the document, will not be parsed [manual entry]
# Uncomment and populate the next lines accordingly
#author_1: Niket Agrawal
#author_2:

# Maintainers of the document, will not be parsed [manual entry]
# Uncomment and populate the next lines accordingly
#maintainer_1: Name Surname
#maintainer_2:

# To whom reach out regarding the document, will not be parsed [manual entry]
# Uncomment and populate the next line accordingly
#corresponding: Name Surname

# Meaningful keywords, newline separated [manual entry]
# Uncomment and populate the next line and list accordingly
categories: 
- testing 
- Python

---

## Writing integration tests in Python


This guide is to help you write a high level test for your code base. 

### Look at your software from 100 feet above the ground

When you are writing a high level test, you are looking at your software from 100 feet above the ground. You are not concerned about the nitty gritty details of the code, but you are concerned about the overall behavior of the software. 


Guide for writing integration test for programs that take input and produce output. 
This guide is suitable for writing tests for programs that take input and produce output.


### Context

Goals of this section is two folds
- On board yourself to someone else’s code
- Write a high level test for an existing code base that covers major scenarios

Key message we want to convey with this section
- Writing a high level (integration) test as the first test for the code can help you
- Learn more about your code or someone else’s code (as a RSE)
- A test that tests the most important parts of your code and good enough for CI


Steps

Issue template with question
Filter to test cases and the input combinations they must be run on. For robustness, you may want to have multiple input combinations you want to run the test cases through. 

Tip: group related test cases under a class so they are more easily readable

Tip: pytest output should clearly show the pass fail status of the test cases and the inputs they run for. This will tell clearly which test cases have run for which inputs and easier to spot for which input they failed. Parametrization provides features to attach aliases/nicknames to label each input (this is handy especially if inputs are long filenames) 


recommendation/tip: use parametrization to specify inputs for test cases. Recommended alternative to for loop, because each test case gets a fresh environment when taking on new input. Parametrization keeps number of lines of code minimal and aids in readability, also easier to add, modify or remove test cases



### GitHub issue template



### Integration test examples from Obelix and Aeolis

#### Obelix
Issue containing test plan: [link](https://github.com/openearth/aeolis-python/issues/60)
Test source code: [link]()


#### Aeolis
Issue containing test plan: [link]()
Test source code: [link]()


### Summary
- Writing a high level test as the first test for the code can help you learn more about your code or someone else’s code (as a RSE). 
- Create a test plan first. Identify the test cases and scenarios you want to test. Using a github issue template with questions can help you identify the test cases and scenarios you want to test.
- Treat your code as a black box when writing high level tests. Think what inputs you can give to the code and what outputs you expect from the code. Focus on the most important part of the code and ask youself what is it supposed to do. 
- Scenarios and test cases. Document scenarios and test cases in a github issue template.
- Work your test backwards. Think of what would you like the test output to tell you, and then write the test. 
- Parametrization helps to keep the code lean and readable. It also helps to add, modify or remove test cases easily.