---
title: get_ToaCategories
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the table of authorities categories.
type: docs
weight: 222
url: /cpp/aspose.words.fields/fieldoptions/get_toacategories/
---
## FieldOptions.get_ToaCategories method


Gets or sets the table of authorities categories.

```cpp
const System::SharedPtr<Aspose::Words::Fields::ToaCategories> & Aspose::Words::Fields::FieldOptions::get_ToaCategories() const
```


## Examples




Shows how to specify a set of categories for TOA fields. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// TOA fields can filter their entries by categories defined in this collection.
auto toaCategories = MakeObject<ToaCategories>();
doc->get_FieldOptions()->set_ToaCategories(toaCategories);

// This collection of categories comes with default values, which we can overwrite with custom values.
ASSERT_EQ(u"Cases", toaCategories->idx_get(1));
ASSERT_EQ(u"Statutes", toaCategories->idx_get(2));

toaCategories->idx_set(1, u"My Category 1");
toaCategories->idx_set(2, u"My Category 2");

// We can always access the default values via this collection.
ASSERT_EQ(u"Cases", ToaCategories::get_DefaultCategories()->idx_get(1));
ASSERT_EQ(u"Statutes", ToaCategories::get_DefaultCategories()->idx_get(2));

// Insert 2 TOA fields. TOA fields create an entry for each TA field in the document.
// Use the "\c" switch to select the index of a category from our collection.
//  With this switch, a TOA field will only pick up entries from TA fields that
// also have a "\c" switch with a matching category index. Each TOA field will also display
// the name of the category that its "\c" switch points to.
builder->InsertField(u"TOA \\c 1 \\h", nullptr);
builder->InsertField(u"TOA \\c 2 \\h", nullptr);
builder->InsertBreak(BreakType::PageBreak);

// Insert TOA entries across 2 categories. Our first TOA field will receive one entry,
// from the second TA field whose "\c" switch also points to the first category.
// The second TOA field will have two entries from the other two TA fields.
builder->InsertField(u"TA \\c 2 \\l \"entry 1\"");
builder->InsertBreak(BreakType::PageBreak);
builder->InsertField(u"TA \\c 1 \\l \"entry 2\"");
builder->InsertBreak(BreakType::PageBreak);
builder->InsertField(u"TA \\c 2 \\l \"entry 3\"");

doc->UpdateFields();
doc->Save(ArtifactsDir + u"FieldOptions.TOA.Categories.docx");
```

