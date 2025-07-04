---
title: IComparisonExpressionEvaluator Interface
linktitle: IComparisonExpressionEvaluator
articleTitle: IComparisonExpressionEvaluator
second_title: Aspose.Words for .NET
description: Enhance your document processing with Aspose.Words.Fields.IComparisonExpressionEvaluator. Customize comparison evaluations for FieldIf and FieldCompare fields effortlessly!
type: docs
weight: 3080
url: /net/aspose.words.fields/icomparisonexpressionevaluator/
---
## IComparisonExpressionEvaluator interface

When implemented, allows to override default comparison expressions evaluation for the [`FieldIf`](../fieldif/) and [`FieldCompare`](../fieldcompare/) fields.

```csharp
public interface IComparisonExpressionEvaluator
```

## Methods

| Name | Description |
| --- | --- |
| [Evaluate](../../aspose.words.fields/icomparisonexpressionevaluator/evaluate/)(*[Field](../field/), [ComparisonExpression](../comparisonexpression/)*) | Evaluates comparison expression. |

## Examples

Shows how to implement custom evaluation for the IF and COMPARE fields.

```csharp
public void ConditionEvaluationExtensionPoint(string fieldCode, sbyte comparisonResult, string comparisonError,
    string expectedResult)
{
    const string left = "\"left expression\"";
    const string @operator = "<>";
    const string right = "\"right expression\"";

    DocumentBuilder builder = new DocumentBuilder();

    // Field codes that we use in this example:
    // 1.   " IF {0} {1} {2} \"true argument\" \"false argument\" ".
    // 2.   " COMPARE {0} {1} {2} ".
    Field field = builder.InsertField(string.Format(fieldCode, left, @operator, right), null);

    // If the "comparisonResult" is undefined, we create "ComparisonEvaluationResult" with string, instead of bool.
    ComparisonEvaluationResult result = comparisonResult != -1
        ? new ComparisonEvaluationResult(comparisonResult == 1)
        : comparisonError != null ? new ComparisonEvaluationResult(comparisonError) : null;

    ComparisonExpressionEvaluator evaluator = new ComparisonExpressionEvaluator(result);
    builder.Document.FieldOptions.ComparisonExpressionEvaluator = evaluator;

    builder.Document.UpdateFields();

    Assert.That(field.Result, Is.EqualTo(expectedResult));
    evaluator.AssertInvocationsCount(1).AssertInvocationArguments(0, left, @operator, right);
}

/// <summary>
/// Comparison expressions evaluation for the FieldIf and FieldCompare.
/// </summary>
private class ComparisonExpressionEvaluator : IComparisonExpressionEvaluator
{
    public ComparisonExpressionEvaluator(ComparisonEvaluationResult result)
    {
        mResult = result;
        if (mResult != null)
        {
            Console.WriteLine(mResult.ErrorMessage);
            Console.WriteLine(mResult.Result);
        }
    }

    public ComparisonEvaluationResult Evaluate(Field field, ComparisonExpression expression)
    {
        mInvocations.Add(new[]
        {
            expression.LeftExpression,
            expression.ComparisonOperator,
            expression.RightExpression
        });

        return mResult;
    }

    public ComparisonExpressionEvaluator AssertInvocationsCount(int expected)
    {
        Assert.That(mInvocations.Count, Is.EqualTo(expected));
        return this;
    }

    public ComparisonExpressionEvaluator AssertInvocationArguments(
        int invocationIndex,
        string expectedLeftExpression,
        string expectedComparisonOperator,
        string expectedRightExpression)
    {
        string[] arguments = mInvocations[invocationIndex];

        Assert.That(arguments[0], Is.EqualTo(expectedLeftExpression));
        Assert.That(arguments[1], Is.EqualTo(expectedComparisonOperator));
        Assert.That(arguments[2], Is.EqualTo(expectedRightExpression));

        return this;
    }

    private readonly ComparisonEvaluationResult mResult;
    private readonly List<string[]> mInvocations = new List<string[]>();
}
```

### See Also

* property [ComparisonExpressionEvaluator](../fieldoptions/comparisonexpressionevaluator/)
* namespace [Aspose.Words.Fields](../../aspose.words.fields/)
* assembly [Aspose.Words](../../)
