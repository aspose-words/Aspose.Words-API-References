---
title: "ComparisonEvaluationResult"
linktitle: "ComparisonEvaluationResult"
second_title: "Aspose.Words Java için"
description: "Java'daki karşılaştırma değerlendirme sonucu."
type: docs
weight: 116
url: /tr/java/com.aspose.words/comparisonevaluationresult/
---

**Inheritance:**
java.lang.Object
```
public class ComparisonEvaluationResult
```

Karşılaştırma değerlendirme sonucu.

Daha fazla bilgi için, [ Working with Fields ][Working with Fields] dokümantasyon makalesini ziyaret edin.

 **Examples:** 

IF ve COMPARE alanları için özel değerlendirme nasıl uygulanır gösterir.

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
## Yapıcılar

| Yapıcı | Açıklama |
| --- | --- |
| [ComparisonEvaluationResult(boolean result)](#ComparisonEvaluationResult-boolean) | Bir karşılaştırma değerlendirme sonucu oluşturur. |
| [ComparisonEvaluationResult(String errorMessage)](#ComparisonEvaluationResult-java.lang.String) | İlgili hata mesajı ile başarısız bir karşılaştırma değerlendirme sonucu oluşturur. |
## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| [getErrorMessage()](#getErrorMessage) | Başarısız karşılaştırma değerlendirme sonucunun hata mesajını alır. |
| [getResult()](#getResult) | Karşılaştırma değerlendirme sonucunu alır. |
### ComparisonEvaluationResult(boolean result) {#ComparisonEvaluationResult-boolean}
```
public ComparisonEvaluationResult(boolean result)
```


Bir karşılaştırma değerlendirme sonucu oluşturur.

 **Examples:** 

IF ve COMPARE alanları için özel değerlendirme nasıl uygulanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| sonuç | boolean |  |

### ComparisonEvaluationResult(String errorMessage) {#ComparisonEvaluationResult-java.lang.String}
```
public ComparisonEvaluationResult(String errorMessage)
```


İlgili hata mesajı ile başarısız bir karşılaştırma değerlendirme sonucu oluşturur.

 **Examples:** 

IF ve COMPARE alanları için özel değerlendirme nasıl uygulanır gösterir.

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
| Parametre | Tür | Açıklama |
| --- | --- | --- |
| errorMessage | java.lang.String |  |

### getErrorMessage() {#getErrorMessage}
```
public String getErrorMessage()
```


Başarısız karşılaştırma değerlendirme sonucunun hata mesajını alır.

 **Examples:** 

IF ve COMPARE alanları için özel değerlendirme nasıl uygulanır gösterir.

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
java.lang.String - Başarısız karşılaştırma değerlendirme sonucunun hata mesajı.
### getResult() {#getResult}
```
public boolean getResult()
```


Karşılaştırma değerlendirme sonucunu alır.

 **Examples:** 

IF ve COMPARE alanları için özel değerlendirme nasıl uygulanır gösterir.

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
boolean - Karşılaştırma değerlendirme sonucu.
