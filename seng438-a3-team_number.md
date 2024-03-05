**SENG 438 - Software Testing, Reliability, and Quality**

**Lab. Report #3 – Code Coverage, Adequacy Criteria and Test Case Correlation**

| Group \#:      |   17  |
| -------------- | --- |
| Student Names: |Rohan Kapila|
|                |Qazi Ali|
|                |Fayzan Toor|
|                |Shayyan Asim|

(Note that some labs require individual reports while others require one report
for each group. Please see each lab document for details.)

# 1 Introduction

In this lab we dove into the coverage matrix and analyzed Instruction Coverage, Branch Coverage, Lines Coverage, Method Cover, Complexity Coverage, and Types Coverage using the EclEmma Coverage tools. Given these tools we were able to learn more about testing methods and enhance our programs. 


# 2 Manual data-flow coverage calculations for X and Y methods
## Range
![DFG](https://github.com/seng438-winter-2024/seng438-a3-QaziSaboorr/assets/113058986/e5f4a536-d0b2-4ea2-91e8-2e84cee99c5c)

![du-pairs](https://github.com/seng438-winter-2024/seng438-a3-QaziSaboorr/assets/113058986/21ae0e27-7235-40e8-af85-25ac9970c1aa)


# 3 A detailed description of the testing strategy for the new unit test

## Range
Detailed Testing Strategy for Selected New Unit Tests
1. testConstructorWithInvalidBounds
Objective: Ensure the Range constructor throws an IllegalArgumentException when given a lower bound greater than the upper bound.
Method Under Test: Range(double lower, double upper)
Strategy:
Invoke the constructor with a lower bound greater than the upper bound (e.g., new Range(2, 1)).
Use JUnit's expected exception mechanism to verify that an IllegalArgumentException is thrown.
This test directly increases method and statement coverage by exercising constructor validation logic.
2. testGetLength
Objective: Verify that the getLength method accurately calculates the length of the range.
Method Under Test: getLength()
Strategy:
Create ranges with known lengths (including zero and positive values).
Assert that getLength returns the correct value for each range.
This test increases statement coverage by exercising the calculation path within getLength.
3. testShiftWithExtremeDelta
Objective: Examine the behavior of the shift method when shifting a range by extremely large positive and negative deltas.
Method Under Test: shift(Range base, double delta, boolean allowZeroCrossing)
Strategy:
Shift a range by Double.MAX_VALUE and -Double.MAX_VALUE to test the handling of extreme values.
Verify that the resulting range's bounds are correctly adjusted, including checks for infinity bounds if applicable.
This test contributes to branch coverage by covering code paths that handle large shifts, potentially testing overflow behavior.
4. testCombineRangeWithItself
Objective: Confirm that combining a range with itself returns a range equal to the original.
Method Under Test: combine(Range range1, Range range2)
Strategy:
Combine a range with itself and verify that the result is equal to the original range.
This test enhances method and statement coverage, particularly testing the idempotency of the combine method.
5. testContainsValueBelowLowerBound
Objective: Test the contains method to ensure it correctly identifies values below the range's lower bound.
Method Under Test: contains(double value)
Strategy:
Use a range and test with a value below its lower bound, asserting that contains returns false.
This test improves branch coverage by ensuring conditions checking if a value is within the range are correctly evaluated.

# 4 A high level description of five selected test cases you have designed using coverage information, and how they have increased code coverage

Text…

# 5 A detailed report of the coverage achieved of each class and method (a screen shot from the code cover results in green and red color would suffice)

## Ranges
![Image 2024-03-04 at 8 57 PM](https://github.com/seng438-winter-2024/seng438-a3-QaziSaboorr/assets/113058986/85da91d9-5e3a-48fc-aab7-6cedf087e85f)
![C1BB1FAE-3C5A-4A77-AA48-6918EB9A656A](https://github.com/seng438-winter-2024/seng438-a3-QaziSaboorr/assets/113058986/b5422410-8a1e-416a-9c7a-cb89d3503f8f)

In the above context we werent able to retrieve a statment coverage, due to the constructor class. The constructor class initially checks if the lower bound is greater than the upper bound. In the conceding methods we werent able to check some of the statments due to this requirment already being met. This results in us not being able to use these statments and lowering pur statment coverage. This is demonstrated in the image above.


# 6 Pros and Cons of coverage tools used and Metrics you report

Text…

# 7 A comparison on the advantages and disadvantages of requirements-based test generation and coverage-based test generation.

Text…

# 8 A discussion on how the team work/effort was divided and managed

Text…

# 9 Any difficulties encountered, challenges overcome, and lessons learned from performing the lab

Text…

# 10 Comments/feedback on the lab itself

Text…
