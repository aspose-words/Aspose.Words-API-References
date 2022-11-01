---
title: get_Location
second_title: Aspose.Words for C++ API Reference
description: Gets or sets the name of a bookmark, a page number, or some other item to jump to.
type: docs
weight: 14
url: /cpp/aspose.words.fields/fieldgotobutton/get_location/
---
## FieldGoToButton.get_Location method


Gets or sets the name of a bookmark, a page number, or some other item to jump to.

```cpp
System::String Aspose::Words::Fields::FieldGoToButton::get_Location()
```


## Examples




Shows to insert a GOTOBUTTON field. 
```cpp
auto doc = MakeObject<Document>();
auto builder = MakeObject<DocumentBuilder>(doc);

// Add a GOTOBUTTON field. When we double-click this field in Microsoft Word,
// it will take the text cursor to the bookmark whose name the Location property references.
auto field = System::DynamicCast<FieldGoToButton>(builder->InsertField(FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// Insert a valid bookmark for the field to reference.
builder->InsertBreak(BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(ArtifactsDir + u"Field.GOTOBUTTON.docx");
```

