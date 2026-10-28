---
title: Aspose::Words::Fields::FieldGoToButton::set_Location method
linktitle: set_Location
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fields::FieldGoToButton::set_Location method. Sets the name of a bookmark, a page number, or some other item to jump to in C++.'
type: docs
weight: 7000
url: /cpp/aspose.words.fields/fieldgotobutton/set_location/
---
## FieldGoToButton::set_Location method


Sets the name of a bookmark, a page number, or some other item to jump to.

```cpp
void Aspose::Words::Fields::FieldGoToButton::set_Location(const System::String & value)
```

## Examples


Shows to insert a GOTOBUTTON field.

```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Add a GOTOBUTTON field. When we double-click this field in Microsoft Word,
// it will take the text cursor to the bookmark whose name the Location property references.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldGoToButton>(builder->InsertField(FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// Insert a valid bookmark for the field to reference.
builder->InsertBreak(BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.GOTOBUTTON.docx");
```
## See Also

* Class [FieldGoToButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
