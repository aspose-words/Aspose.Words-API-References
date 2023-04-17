---
title: Aspose::Words::Fields::Field::Remove method
linktitle: Remove
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::Field::Remove method. Removes the field from the document. Returns a node right after the field. If the field''s end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns null in C++.'
type: docs
weight: 17000
url: /cpp/aspose.words.fields/field/remove/
---
## Field::Remove method


Removes the field from the document. Returns a node right after the field. If the field's end is the last child of its parent node, returns its parent paragraph. If the field is already removed, returns **null**.

```cpp
System::SharedPtr<Aspose::Words::Node> Aspose::Words::Fields::Field::Remove()
```


## Examples



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


Shows how to process PRIVATE fields. 
```cpp
void FieldPrivate_()
{
    // Open a Corel WordPerfect document which we have converted to .docx format.
    auto doc = MakeObject<Document>(MyDir + u"Field sample - PRIVATE.docx");

    // WordPerfect 5.x/6.x documents like the one we have loaded may contain PRIVATE fields.
    // Microsoft Word preserves PRIVATE fields during load/save operations,
    // but provides no functionality for them.
    auto field = System::DynamicCast<FieldPrivate>(doc->get_Range()->get_Fields()->idx_get(0));

    ASSERT_EQ(u" PRIVATE \"My value\" ", field->GetFieldCode());
    ASSERT_EQ(FieldType::FieldPrivate, field->get_Type());

    // We can also insert PRIVATE fields using a document builder.
    auto builder = MakeObject<DocumentBuilder>(doc);
    builder->InsertField(FieldType::FieldPrivate, true);

    // These fields are not a viable way of protecting sensitive information.
    // Unless backward compatibility with older versions of WordPerfect is essential,
    // we can safely remove these fields. We can do this using a DocumentVisiitor implementation.
    ASSERT_EQ(2, doc->get_Range()->get_Fields()->get_Count());

    auto remover = MakeObject<ExField::FieldPrivateRemover>();
    doc->Accept(remover);

    ASSERT_EQ(2, remover->GetFieldsRemovedCount());
    ASSERT_EQ(0, doc->get_Range()->get_Fields()->get_Count());
}

class FieldPrivateRemover : public DocumentVisitor
{
public:
    FieldPrivateRemover() : mFieldsRemovedCount(0)
    {
        mFieldsRemovedCount = 0;
    }

    int GetFieldsRemovedCount()
    {
        return mFieldsRemovedCount;
    }

    VisitorAction VisitFieldEnd(SharedPtr<FieldEnd> fieldEnd) override
    {
        if (fieldEnd->get_FieldType() == FieldType::FieldPrivate)
        {
            fieldEnd->GetField()->Remove();
            mFieldsRemovedCount++;
        }

        return VisitorAction::Continue;
    }

private:
    int mFieldsRemovedCount;
};
```

## See Also

* Class [Node](../../../aspose.words/node/)
* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
