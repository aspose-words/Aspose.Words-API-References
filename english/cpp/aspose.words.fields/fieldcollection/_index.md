---
title: FieldCollection
second_title: Aspose.Words for C++ API Reference
description: A collection of Field objects that represents the fields in the specified range.
type: docs
weight: 287
url: /cpp/aspose.words.fields/fieldcollection/
---
## FieldCollection class


A collection of [Field](../field/) objects that represents the fields in the specified range.

```cpp
class FieldCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::Fields::Field>>
```

## Methods

| Method | Description |
| --- | --- |
| [Clear](./clear/)() | Removes all fields of this collection from the document and from this collection itself. |
| [get_Count](./get_count/)() | Returns the number of the fields in the collection. |
| [GetEnumerator](./getenumerator/)() override | Returns an enumerator object. |
| [idx_get](./idx_get/)(int32_t) | Returns a field at the specified index. |
| [Remove](./remove/)(const System::SharedPtr\<Aspose::Words::Fields::Field\>\&) | Removes the specified field from this collection and from the document. |
| [RemoveAt](./removeat/)(int32_t) | Removes a field at the specified index from this collection and from the document. |
## Remarks


An instance of this collection iterates fields which start fall within the specified range.

The [FieldCollection](./) collection does not own the fields it contains, rather, is just a selection of fields.

The [FieldCollection](./) collection is "live", i.e. changes to the children of the node object that it was created from are immediately reflected in the fields returned by the [FieldCollection](./) properties and methods.

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


Shows how to remove fields from a field collection. 
```cpp
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

// Below are four ways of removing fields from a field collection.
// 1 -  Get a field to remove itself:
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  Get the collection to remove a field that we pass to its removal method:
SharedPtr<Field> lastField = fields->idx_get(3);
fields->Remove(lastField);
ASSERT_EQ(4, fields->get_Count());

// 3 -  Remove a field from a collection at an index:
fields->RemoveAt(2);
ASSERT_EQ(3, fields->get_Count());

// 4 -  Remove all the fields from the collection at once:
fields->Clear();
ASSERT_EQ(0, fields->get_Count());
```

## See Also

* Namespace [Aspose::Words::Fields](../)
* Library [Aspose.Words](../../)
