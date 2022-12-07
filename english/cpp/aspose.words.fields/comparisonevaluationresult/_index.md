---
title: ComparisonEvaluationResult
second_title: Aspose.Words for C++ API Reference
description: The comparison evaluation result. To learn more, visit the  documentation article.
type: docs
weight: 14
url: /cpp/aspose.words.fields/comparisonevaluationresult/
---
## ComparisonEvaluationResult class


The comparison evaluation result. To learn more, visit the [Working with Fields](https://docs.aspose.com/words/cpp/working-with-fields/) documentation article.

```cpp
class ComparisonEvaluationResult : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| [ComparisonEvaluationResult](./comparisonevaluationresult/)(bool) | Creates a comparison evaluation result. |
| [ComparisonEvaluationResult](./comparisonevaluationresult/)(const System::String\&) | Creates a failed comparison evaluation result with the corresponding error message. |
| [get_ErrorMessage](./get_errormessage/)() const | Gets the failed comparison evaluation result's error message. |
| [get_Result](./get_result/)() const | Gets the comparison evaluation result. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## Examples



Shows how to implement custom evaluation for the IF and COMPARE fields. 
```cpp
void ConditionEvaluationExtensionPoint(String fieldCode, int8_t comparisonResult, String comparisonError, String expectedResult)
{
    const String left = u"\"left expression\"";
    const String operator_ = u"<>";
    const String right = u"\"right expression\"";

    auto builder = MakeObject<DocumentBuilder>();

    // Field codes that we use in this example:
    // 1.   " IF {0} {1} {2} \"true argument\" \"false argument\" ".
    // 2.   " COMPARE {0} {1} {2} ".
    SharedPtr<Field> field = builder->InsertField(String::Format(fieldCode, left, operator_, right), nullptr);

    // If the "comparisonResult" is undefined, we create "ComparisonEvaluationResult" with string, instead of bool.
    SharedPtr<ComparisonEvaluationResult> result = comparisonResult != -1       ? MakeObject<ComparisonEvaluationResult>(comparisonResult == 1)
                                                   : comparisonError != nullptr ? MakeObject<ComparisonEvaluationResult>(comparisonError)
                                                                                : nullptr;

    auto evaluator = MakeObject<ExField::ComparisonExpressionEvaluator>(result);
    builder->get_Document()->get_FieldOptions()->set_ComparisonExpressionEvaluator(evaluator);

    builder->get_Document()->UpdateFields();

    ASSERT_EQ(expectedResult, field->get_Result());
    evaluator->AssertInvocationsCount(1)->AssertInvocationArguments(0, left, operator_, right);
}

class ComparisonExpressionEvaluator : public IComparisonExpressionEvaluator
{
public:
    ComparisonExpressionEvaluator(SharedPtr<ComparisonEvaluationResult> result)
        : mInvocations(MakeObject<System::Collections::Generic::List<ArrayPtr<String>>>())
    {
        mResult = result;
    }

    SharedPtr<ComparisonEvaluationResult> Evaluate(SharedPtr<Field> field, SharedPtr<ComparisonExpression> expression) override
    {
        mInvocations->Add(MakeArray<String>({expression->get_LeftExpression(), expression->get_ComparisonOperator(), expression->get_RightExpression()}));

        return mResult;
    }

    SharedPtr<ExField::ComparisonExpressionEvaluator> AssertInvocationsCount(int expected)
    {
        EXPECT_EQ(expected, mInvocations->get_Count());
        return System::MakeSharedPtr(this);
    }

    SharedPtr<ExField::ComparisonExpressionEvaluator> AssertInvocationArguments(int invocationIndex, String expectedLeftExpression,
                                                                                String expectedComparisonOperator, String expectedRightExpression)
    {
        ArrayPtr<String> arguments = mInvocations->idx_get(invocationIndex);

        EXPECT_EQ(expectedLeftExpression, arguments[0]);
        EXPECT_EQ(expectedComparisonOperator, arguments[1]);
        EXPECT_EQ(expectedRightExpression, arguments[2]);

        return System::MakeSharedPtr(this);
    }

protected:
    virtual ~ComparisonExpressionEvaluator()
    {
    }

private:
    SharedPtr<ComparisonEvaluationResult> mResult;
    SharedPtr<System::Collections::Generic::List<ArrayPtr<String>>> mInvocations;
};
```

## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words](../../)
