# Unit Test Report
## General Information
**Test Stage**: Unit  
**Test Date**: 2020-03-27 (Y-M-D)  
**Tester**: Eldon Lake  
**Test Case Number**: 1  
**Test case description**: Test the financials property of a ticker known to have correct data
**Results**: Pass  
**Incident Number**: [#639](https://github.com/ranaroussi/yfinance/issues/639)  

## Introduction

**Requirements to be tested**: This test requires the python module dill, in addition to the modules listed in requirements.txt  
**Roles and responsibilities**:
| Person | role   |
|--------|--------|
| Eldon | Tester |

**Set Up procedures**: Install dill: pip install dill  
**Hardware**: Any
**Software**: Dill, doctest, unittest  
**Procedural Requirements**: none known

## Test
**Test Items and features**: [quaterly_financial_test.py](/tests/quarterly_financial_test.py)#test_quarterly_financials_is_in_correct_format  
**Input Specifications**: No input  
**Procedural Steps**: This test is run via the unittest module alongisde the negative test when running test_financials.py. To test just this case independently via doctest: python -m yfinance.ticker -v  
**Expected Results of Case**: test_financials should report 2 out of 2 tests passing. If running independently with doctest, it will note that 7 of 7 tests have passed, since each statement is considered a test even if it has no expected output, as producing no output is the test condition for those statements.

## Actual Results
**Output Specifications**: The test passed without issue. Running the test independently with doctest, it provides a runtime warning regarding relative imports, but it does not create any actual problems when executing. Running the tests via the unittest module (test_financials.py) passes without any warnings.