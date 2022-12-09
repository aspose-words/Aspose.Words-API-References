---
title: get_FieldEnd
second_title: Aspose.Words for C++ API Reference
description: Gets the node that represents the field end.
type: docs
weight: 40
url: /cpp/aspose.words.fields/field/get_fieldend/
---
## Field::get_FieldEnd method


Gets the node that represents the field end.

```cpp
System::SharedPtr<Aspose::Words::Fields::FieldEnd> Aspose::Words::Fields::Field::get_FieldEnd() const
```


## Examples



Shows how to work with a collection of fields. 
```cpp
void FieldCollection_()
{
    auto doc = MakeObject<Document>();
    auto builder = MakeObject<DocumentBuilder>(doc);

    builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
    builder->InsertField(u" TIME ");
    builder->InsertField(u" REVNUM ");
    builder->InsertField(u" AUTHOR  \"John Doe\" ");
    builder->InsertField(u" SUBJECT \"My Subject\" ");
    builder->InsertField(u" QUOTE \"Hello world!\" ");
    doc->UpdateFields();

    SharedPtr<FieldCollection> fields = doc->get_Range()->get_Fields();

    ASSERT_EQ(6, fields->get_Count());

    // Iterate over the field collection, and print contents and type
    // of every field using a custom visitor implementation.
    auto fieldVisitor = MakeObject<ExField::FieldVisitor>();

    {
        SharedPtr<System::Collections::Generic::IEnumerator<SharedPtr<Field>>> fieldEnumerator = fields->GetEnumerator();
        while (fieldEnumerator->MoveNext())
        {
            if (fieldEnumerator->get_Current() != nullptr)
            {
                fieldEnumerator->get_Current()->get_Start()->Accept(fieldVisitor);
                if (fieldEnumerator->get_Current()->get_Separator() != nullptr)
                {
                    fieldEnumerator->get_Current()->get_Separator()->Accept(fieldVisitor);
                }
                fieldEnumerator->get_Current()->get_End()->Accept(fieldVisitor);
            }
            else
            {
                std::cout << "There are no fields in the document." << std::endl;
            }
        }
    }

    std::cout << fieldVisitor->GetText() << std::endl;
}

class FieldVisitor : public DocumentVisitor
{
public:
    FieldVisitor()
    {
        mBuilder = MakeObject<System::Text::StringBuilder>();
    }

    String GetText()
    {
        return mBuilder->ToString();
    }

    VisitorAction VisitFieldStart(SharedPtr<FieldStart> fieldStart) override
    {
        mBuilder->AppendLine(String(u"Found field: ") + System::ObjectExt::ToString(fieldStart->get_FieldType()));
        mBuilder->AppendLine(String(u"\tField code: ") + fieldStart->GetField()->GetFieldCode());
        mBuilder->AppendLine(String(u"\tDisplayed as: ") + fieldStart->GetField()->get_Result());

        return VisitorAction::Continue;
    }

    VisitorAction VisitFieldSeparator(SharedPtr<FieldSeparator> fieldSeparator) override
    {
        mBuilder->AppendLine(String(u"\tFound separator: ") + fieldSeparator->GetText());

        return VisitorAction::Continue;
    }

    VisitorAction VisitFieldEnd(SharedPtr<FieldEnd> fieldEnd) override
    {
        mBuilder->AppendLine(String(u"End of field: ") + System::ObjectExt::ToString(fieldEnd->get_FieldType()));

        return VisitorAction::Continue;
    }

private:
    SharedPtr<System::Text::StringBuilder> mBuilder;
};
```

## See Also

* Class [FieldEnd](../../fieldend/)
* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words](../../../)
