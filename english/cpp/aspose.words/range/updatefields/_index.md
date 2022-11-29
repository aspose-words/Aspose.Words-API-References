---
title: UpdateFields
second_title: Aspose.Words for C++ API Reference
description: Updates the values of document fields in this range.
type: docs
weight: 131
url: /cpp/aspose.words/range/updatefields/
---
## Range::UpdateFields method


Updates the values of document fields in this range.

```cpp
void Aspose::Words::Range::UpdateFields()
```

## Remarks


When you open, modify and then save a document, Aspose.Words does not update fields automatically, it keeps them intact. Therefore, you would usually want to call this method before saving if you have modified the document programmatically and want to make sure the proper (calculated) field values appear in the saved document.

There is no need to update fields after executing a mail merge because mail merge is a kind of field update and automatically updates all fields in the document.

This method does not update all field types. For the detailed list of supported field types, see the Programmers Guide.

This method does not update fields that are related to the page layout algorithms (e.g. PAGE, PAGES, PAGEREF). The page layout-related fields are updated when you render a document or call [UpdatePageLayout](../../document/updatepagelayout/).

To update fields in the whole document use [UpdateFields](../../document/updatefields/).

## Examples



Shows how to update all the fields in a range. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

builder->InsertField(u" DOCPROPERTY Category");
builder->InsertBreak(BreakType::SectionBreakEvenPage);
builder->InsertField(u" DOCPROPERTY Category");

// The above DOCPROPERTY fields will display the value of this built-in document property.
doc->get_BuiltInDocumentProperties()->set_Category(u"MyCategory");

// If we update the value of a document property, we will need to update all the DOCPROPERTY fields to display it.
ASSERT_EQ(String::Empty, doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());

// Update all the fields that are in the range of the first section.
doc->get_FirstSection()->get_Range()->UpdateFields();

ASSERT_EQ(u"MyCategory", doc->get_Range()->get_Fields()->idx_get(0)->get_Result());
ASSERT_EQ(String::Empty, doc->get_Range()->get_Fields()->idx_get(1)->get_Result());
```

## See Also

* Class [Range](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words](../../../)
