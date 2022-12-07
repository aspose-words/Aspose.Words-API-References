---
title: get_RightExpression
second_title: Aspose.Words for C++ API Reference
description: Gets the right expression.
type: docs
weight: 40
url: /cpp/aspose.words.fields/comparisonexpression/get_rightexpression/
---
## ComparisonExpression::get_RightExpression method


Gets the right expression.

```cpp
System::String Aspose::Words::Fields::ComparisonExpression::get_RightExpression() const
```


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

* Class [ComparisonExpression](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
