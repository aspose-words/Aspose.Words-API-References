---
title: "ComparisonEvaluationResult"
linktitle: "ComparisonEvaluationResult"
second_title: "Aspose.Words für Java"
description: "Das Vergleichsauswertungsergebnis in Java."
type: docs
weight: 116
url: /de/java/com.aspose.words/comparisonevaluationresult/
---

**Inheritance:**
java.lang.Object
```
public class ComparisonEvaluationResult
```

Das Ergebnis der Vergleichsauswertung.

Weitere Informationen finden Sie im Dokumentationsartikel [ Working with Fields ][Working with Fields].

 **Examples:** 

Zeigt, wie man eine benutzerdefinierte Auswertung für die IF- und COMPARE-Felder implementiert.

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
## Konstruktoren

| Konstruktor | Beschreibung |
| --- | --- |
| [ComparisonEvaluationResult(boolean result)](#ComparisonEvaluationResult-boolean) | Erstellt ein Vergleichsauswertungsergebnis. |
| [ComparisonEvaluationResult(String errorMessage)](#ComparisonEvaluationResult-java.lang.String) | Erstellt ein fehlgeschlagenes Vergleichsauswertungsergebnis mit der entsprechenden Fehlermeldung. |
## Methoden

| Methode | Beschreibung |
| --- | --- |
| [getErrorMessage()](#getErrorMessage) | Ermittelt die Fehlermeldung des fehlgeschlagenen Vergleichsauswertungsergebnisses. |
| [getResult()](#getResult) | Ermittelt das Vergleichsauswertungsergebnis. |
### ComparisonEvaluationResult(boolean result) {#ComparisonEvaluationResult-boolean}
```
public ComparisonEvaluationResult(boolean result)
```


Erstellt ein Vergleichsauswertungsergebnis.

 **Examples:** 

Zeigt, wie man eine benutzerdefinierte Auswertung für die IF- und COMPARE-Felder implementiert.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Ergebnis | boolean |  |

### ComparisonEvaluationResult(String errorMessage) {#ComparisonEvaluationResult-java.lang.String}
```
public ComparisonEvaluationResult(String errorMessage)
```


Erstellt ein fehlgeschlagenes Vergleichsauswertungsergebnis mit der entsprechenden Fehlermeldung.

 **Examples:** 

Zeigt, wie man eine benutzerdefinierte Auswertung für die IF- und COMPARE-Felder implementiert.

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

**Parameters:**
| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| Fehlermeldung | java.lang.String |  |

### getErrorMessage() {#getErrorMessage}
```
public String getErrorMessage()
```


Ermittelt die Fehlermeldung des fehlgeschlagenen Vergleichsauswertungsergebnisses.

 **Examples:** 

Zeigt, wie man eine benutzerdefinierte Auswertung für die IF- und COMPARE-Felder implementiert.

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

**Returns:**
java.lang.String – Die Fehlermeldung des fehlgeschlagenen Vergleichsauswertungsergebnisses.
### getResult() {#getResult}
```
public boolean getResult()
```


Ermittelt das Vergleichsauswertungsergebnis.

 **Examples:** 

Zeigt, wie man eine benutzerdefinierte Auswertung für die IF- und COMPARE-Felder implementiert.

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

**Returns:**
boolean – Das Vergleichsauswertungsergebnis.
