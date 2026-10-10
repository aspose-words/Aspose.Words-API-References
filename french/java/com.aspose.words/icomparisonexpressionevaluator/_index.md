---
title: "IComparisonExpressionEvaluator"
linktitle: "IComparisonExpressionEvaluator"
second_title: "Aspose.Words pour Java"
description: "Lorsqu'elle est implémentée, permet de remplacer l'évaluation par défaut des expressions de comparaison pour les champs FieldIf et FieldCompare en Java."
type: docs
weight: 755
url: /fr/java/com.aspose.words/icomparisonexpressionevaluator/
---
```
public interface IComparisonExpressionEvaluator
```

Lorsqu'elle est implémentée, permet de remplacer l'évaluation par défaut des expressions de comparaison pour les champs [FieldIf](../../com.aspose.words/fieldif/) et [FieldCompare](../../com.aspose.words/fieldcompare/).

 **Examples:** 

Montre comment implémenter une évaluation personnalisée pour les champs IF et COMPARE.

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
## Méthodes

| Méthode | Description |
| --- | --- |
| [evaluate(Field field, ComparisonExpression expression)](#evaluate-com.aspose.words.Field-com.aspose.words.ComparisonExpression) | Évalue l'expression de comparaison. |
### evaluate(Field field, ComparisonExpression expression) {#evaluate-com.aspose.words.Field-com.aspose.words.ComparisonExpression}
```
public abstract ComparisonEvaluationResult evaluate(Field field, ComparisonExpression expression)
```


Évalue l'expression de comparaison.

 **Remarks:** 

L'implémentation doit renvoyer  null  pour indiquer que l'évaluation par défaut doit être effectuée.

 **Examples:** 

Montre comment implémenter une évaluation personnalisée pour les champs IF et COMPARE.

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
| Paramètre | Type | Description |
| --- | --- | --- |
| field | [Field](../../com.aspose.words/field/) |  |
| expression | [ComparisonExpression](../../com.aspose.words/comparisonexpression/) |  |

**Returns:**
[ComparisonEvaluationResult](../../com.aspose.words/comparisonevaluationresult/)
