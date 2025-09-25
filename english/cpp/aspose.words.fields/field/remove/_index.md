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
virtual System::SharedPtr<Aspose::Words::Node> Aspose::Words::Fields::Field::Remove()
```


## Examples



Shows how to remove fields from a field collection. 
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->InsertField(u" DATE \\@ \"dddd, d MMMM yyyy\" ");
builder->InsertField(u" TIME ");
builder->InsertField(u" REVNUM ");
builder->InsertField(u" AUTHOR  \"John Doe\" ");
builder->InsertField(u" SUBJECT \"My Subject\" ");
builder->InsertField(u" QUOTE \"Hello world!\" ");
doc->UpdateFields();

System::SharedPtr<Aspose::Words::Fields::FieldCollection> fields = doc->get_Range()->get_Fields();

ASSERT_EQ(6, fields->get_Count());

// Below are four ways of removing fields from a field collection.
// 1 -  Get a field to remove itself:
fields->idx_get(0)->Remove();
ASSERT_EQ(5, fields->get_Count());

// 2 -  Get the collection to remove a field that we pass to its removal method:
System::SharedPtr<Aspose::Words::Fields::Field> lastField = fields->idx_get(3);
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

* Class [Node](../../../aspose.words/node/)
* Class [Field](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
