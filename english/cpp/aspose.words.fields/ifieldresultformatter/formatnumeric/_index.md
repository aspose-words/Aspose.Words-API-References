---
title: FormatNumeric
second_title: Aspose.Words for C++ API Reference
description: Called when Aspose.Words applies a numeric format switch, i.e. \# "#.##".
type: docs
weight: 40
url: /cpp/aspose.words.fields/ifieldresultformatter/formatnumeric/
---
## IFieldResultFormatter::FormatNumeric method


Called when Aspose.Words applies a numeric format switch, i.e. \# "#.##".

```cpp
virtual System::String Aspose::Words::Fields::IFieldResultFormatter::FormatNumeric(double value, System::String format)=0
```


## Examples



Shows how to automatically apply a custom format to field results as the fields are updated. 
```cpp
void FieldResultFormatting_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);
    auto formatter = MakeObject<ExDocumentBuilder::FieldResultFormatter>(u"${0}", u"Date: {0}", u"Item # {0}:");
    doc->get_FieldOptions()->set_ResultFormatter(formatter);

    // Our field result formatter applies a custom format to newly created fields of three types of formats.
    // Field result formatters apply new formatting to fields as they are updated,
    // which happens as soon as we create them using this InsertField method overload.
    // 1 -  Numeric:
    builder->InsertField(u" = 2 + 3 \\# $###");

    ASSERT_EQ(u"$5", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
    ASSERT_EQ(1, formatter->CountFormatInvocations(ApiExamples::ExDocumentBuilder::FieldResultFormatter::FormatInvocationType::Numeric));

    // 2 -  Date/time:
    builder->InsertField(u"DATE \\@ \"d MMMM yyyy\"");

    ASSERT_TRUE(doc->get_Range()->get_Fields()->idx_get(1)->get_Result().StartsWith(u"Date: "));
    ASSERT_EQ(1, formatter->CountFormatInvocations(ApiExamples::ExDocumentBuilder::FieldResultFormatter::FormatInvocationType::DateTime));

    // 3 -  General:
    builder->InsertField(u"QUOTE \"2\" \\* Ordinal");

    ASSERT_EQ(u"Item # 2:", doc->get_Range()->get_Fields()->idx_get(2)->get_Result());
    ASSERT_EQ(1, formatter->CountFormatInvocations(ApiExamples::ExDocumentBuilder::FieldResultFormatter::FormatInvocationType::General));

    formatter->PrintFormatInvocations();
}

class FieldResultFormatter : public IFieldResultFormatter
{
public:
    enum class FormatInvocationType
    {
        Numeric,
        DateTime,
        General,
        All
    };

private:
    class FormatInvocation : public System::Object
    {
    public:
        ApiExamples::ExDocumentBuilder::FieldResultFormatter::FormatInvocationType get_FormatInvocationType()
        {
            return pr_FormatInvocationType;
        }

        SharedPtr<System::Object> get_Value()
        {
            return pr_Value;
        }

        String get_OriginalFormat()
        {
            return pr_OriginalFormat;
        }

        String get_NewValue()
        {
            return pr_NewValue;
        }

        FormatInvocation(ApiExamples::ExDocumentBuilder::FieldResultFormatter::FormatInvocationType formatInvocationType, SharedPtr<System::Object> value,
                         String originalFormat, String newValue)
            : pr_FormatInvocationType(((ApiExamples::ExDocumentBuilder::FieldResultFormatter::FormatInvocationType)0))
        {
            pr_Value = value;
            pr_FormatInvocationType = formatInvocationType;
            pr_OriginalFormat = originalFormat;
            pr_NewValue = newValue;
        }

    private:
        ApiExamples::ExDocumentBuilder::FieldResultFormatter::FormatInvocationType pr_FormatInvocationType;
        SharedPtr<System::Object> pr_Value;
        String pr_OriginalFormat;
        String pr_NewValue;
    };

public:
    FieldResultFormatter(String numberFormat, String dateFormat, String generalFormat)
        : mFormatInvocations(MakeObject<System::Collections::Generic::List<SharedPtr<ExDocumentBuilder::FieldResultFormatter::FormatInvocation>>>())
    {
        mNumberFormat = numberFormat;
        mDateFormat = dateFormat;
        mGeneralFormat = generalFormat;
    }

    String FormatNumeric(double value, String format) override
    {
        if (String::IsNullOrEmpty(mNumberFormat))
        {
            return nullptr;
        }

        String newValue = String::Format(mNumberFormat, value);
        get_FormatInvocations()->Add(MakeObject<ExDocumentBuilder::FieldResultFormatter::FormatInvocation>(
            ApiExamples::ExDocumentBuilder::FieldResultFormatter::FormatInvocationType::Numeric, System::ObjectExt::Box<double>(value), format, newValue));
        return newValue;
    }

    String FormatDateTime(System::DateTime value, String format, CalendarType calendarType) override
    {
        if (String::IsNullOrEmpty(mDateFormat))
        {
            return nullptr;
        }

        String newValue = String::Format(mDateFormat, value);
        get_FormatInvocations()->Add(MakeObject<ExDocumentBuilder::FieldResultFormatter::FormatInvocation>(
            ApiExamples::ExDocumentBuilder::FieldResultFormatter::FormatInvocationType::DateTime,
            System::ObjectExt::Box<String>(String::Format(u"{0} ({1})", value, calendarType)), format, newValue));
        return newValue;
    }

    String Format(String value, GeneralFormat format) override
    {
        return Format(System::ObjectExt::Box<String>(value), format);
    }

    String Format(double value, GeneralFormat format) override
    {
        return Format(System::ObjectExt::Box<double>(value), format);
    }

    int CountFormatInvocations(ExDocumentBuilder::FieldResultFormatter::FormatInvocationType formatInvocationType)
    {
        if (formatInvocationType == ApiExamples::ExDocumentBuilder::FieldResultFormatter::FormatInvocationType::All)
        {
            return get_FormatInvocations()->get_Count();
        }

        std::function<bool(SharedPtr<FormatInvocation> f)> hasValidFormatInvocationType = [&formatInvocationType](SharedPtr<FormatInvocation> f)
        {
            return f->get_FormatInvocationType() == formatInvocationType;
        };

        return get_FormatInvocations()->LINQ_Count(hasValidFormatInvocationType);
    }

    void PrintFormatInvocations()
    {
        for (const auto& f : get_FormatInvocations())
        {
            std::cout << (String::Format(u"Invocation type:\t{0}\n", f->get_FormatInvocationType()) +
                          String::Format(u"\tOriginal value:\t\t{0}\n", f->get_Value()) +
                          String::Format(u"\tOriginal format:\t{0}\n", f->get_OriginalFormat()) +
                          String::Format(u"\tNew value:\t\t\t{0}\n", f->get_NewValue()))
                      << std::endl;
        }
    }

private:
    String mNumberFormat;
    String mDateFormat;
    String mGeneralFormat;
    SharedPtr<System::Collections::Generic::List<SharedPtr<ExDocumentBuilder::FieldResultFormatter::FormatInvocation>>> mFormatInvocations;

    SharedPtr<System::Collections::Generic::List<SharedPtr<ExDocumentBuilder::FieldResultFormatter::FormatInvocation>>> get_FormatInvocations()
    {
        return mFormatInvocations;
    }

    String Format(SharedPtr<System::Object> value, GeneralFormat format)
    {
        if (String::IsNullOrEmpty(mGeneralFormat))
        {
            return nullptr;
        }

        String newValue = String::Format(mGeneralFormat, value);
        get_FormatInvocations()->Add(MakeObject<ExDocumentBuilder::FieldResultFormatter::FormatInvocation>(
            ApiExamples::ExDocumentBuilder::FieldResultFormatter::FormatInvocationType::General, value, System::ObjectExt::ToString(format), newValue));
        return newValue;
    }
};
```

## See Also

* Interface [IFieldResultFormatter](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
