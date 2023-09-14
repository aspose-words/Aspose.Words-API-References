---
title: ComparisonEvaluationResult
linktitle: ComparisonEvaluationResult
second_title: Aspose.Words for Java
description: The comparison evaluation result in Java.
type: docs
weight: 96
url: /java/com.aspose.words/comparisonevaluationresult/
---

**Inheritance:**
java.lang.Object
```
public class ComparisonEvaluationResult
```

The comparison evaluation result.

To learn more, visit the [ Working with Fields ][Working with Fields] documentation article.

 **Examples:** 

Shows how to implement custom evaluation for the IF and COMPARE fields.

```

 public void conditionEvaluationExtensionPoint(String fieldCode, byte comparisonResult, String comparisonError,
                                               String expectedResult) throws Exception {
     final String LEFT = "\"left expression\"";
     final String _OPERATOR = "<>";
     final String RIGHT = "\"right expression\"";

     DocumentBuilder builder = new DocumentBuilder();

     // Field codes that we use in this example:
     // 1.   " IF %s %s %s \"true argument\" \"false argument\" ".
     // 2.   " COMPARE %s %s %s ".
     Field field = builder.insertField(String.format(fieldCode, LEFT, _OPERATOR, RIGHT), null);

     // If the "comparisonResult" is undefined, we create "ComparisonEvaluationResult" with string, instead of bool.
     ComparisonEvaluationResult result = comparisonResult != -1
             ? new ComparisonEvaluationResult(comparisonResult == 1)
             : comparisonError != null ? new ComparisonEvaluationResult(comparisonError) : null;

     ComparisonExpressionEvaluator evaluator = new ComparisonExpressionEvaluator(result);
     builder.getDocument().getFieldOptions().setComparisonExpressionEvaluator(evaluator);

     builder.getDocument().updateFields();

     Assert.assertEquals(expectedResult, field.getResult());
     evaluator.assertInvocationsCount(1).assertInvocationArguments(0, LEFT, _OPERATOR, RIGHT);
 }

 public static Object[][] conditionEvaluationExtensionPointDataProvider() {
     return new Object[][]
             {
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) 1, null, "true argument"},
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) 0, null, "false argument"},
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) -1, "Custom Error", "Custom Error"},
                     {" IF %s %s %s \"true argument\" \"false argument\" ", (byte) -1, null, "true argument"},
                     {" COMPARE %s %s %s ", (byte) 1, null, "1"},
                     {" COMPARE %s %s %s ", (byte) 0, null, "0"},
                     {" COMPARE %s %s %s ", (byte) -1, "Custom Error", "Custom Error"},
                     {" COMPARE %s %s %s ", (byte) -1, null, "1"},
             };
 }

 /// 
 /// Comparison expressions evaluation for the FieldIf and FieldCompare.
 /// 
 private static class ComparisonExpressionEvaluator implements IComparisonExpressionEvaluator {
     public ComparisonExpressionEvaluator(ComparisonEvaluationResult result) {
         mResult = result;
     }

     public ComparisonEvaluationResult evaluate(Field field, ComparisonExpression expression) {
         mInvocations.add(new String[]
                 {
                         expression.getLeftExpression(),
                         expression.getComparisonOperator(),
                         expression.getRightExpression()
                 });

         return mResult;
     }

     public ComparisonExpressionEvaluator assertInvocationsCount(int expected) {
         Assert.assertEquals(expected, mInvocations.size());
         return this;
     }

     public ComparisonExpressionEvaluator assertInvocationArguments(
             int invocationIndex,
             String expectedLeftExpression,
             String expectedComparisonOperator,
             String expectedRightExpression) {
         String[] arguments = mInvocations.get(invocationIndex);

         Assert.assertEquals(expectedLeftExpression, arguments[0]);
         Assert.assertEquals(expectedComparisonOperator, arguments[1]);
         Assert.assertEquals(expectedRightExpression, arguments[2]);

         return this;
     }

     private final ComparisonEvaluationResult mResult;
     private final ArrayList mInvocations = new ArrayList<>();
 }
 
```


[Working with Fields]: https://docs.aspose.com/words/java/working-with-fields/
## Constructors

| Constructor | Description |
| --- | --- |
| [ComparisonEvaluationResult(boolean result)](#ComparisonEvaluationResult-boolean) | Creates a comparison evaluation result. |
| [ComparisonEvaluationResult(String errorMessage)](#ComparisonEvaluationResult-java.lang.String) | Creates a failed comparison evaluation result with the corresponding error message. |
## Methods

| Method | Description |
| --- | --- |
| [getErrorMessage()](#getErrorMessage) | Gets the failed comparison evaluation result's error message. |
| [getResult()](#getResult) | Gets the comparison evaluation result. |
### ComparisonEvaluationResult(boolean result) {#ComparisonEvaluationResult-boolean}
```
public ComparisonEvaluationResult(boolean result)
```


Creates a comparison evaluation result.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| result | boolean |  |

### ComparisonEvaluationResult(String errorMessage) {#ComparisonEvaluationResult-java.lang.String}
```
public ComparisonEvaluationResult(String errorMessage)
```


Creates a failed comparison evaluation result with the corresponding error message.

**Parameters:**
| Parameter | Type | Description |
| --- | --- | --- |
| errorMessage | java.lang.String |  |

### getErrorMessage() {#getErrorMessage}
```
public String getErrorMessage()
```


Gets the failed comparison evaluation result's error message.

**Returns:**
java.lang.String - The failed comparison evaluation result's error message.
### getResult() {#getResult}
```
public boolean getResult()
```


Gets the comparison evaluation result.

**Returns:**
boolean - The comparison evaluation result.
