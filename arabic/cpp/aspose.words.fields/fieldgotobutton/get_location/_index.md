---
title: "Aspose::Words::Fields::FieldGoToButton::get_Location طريقة"
linktitle: "get_Location"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Fields::FieldGoToButton::get_Location طريقة. يحصل أو يضبط اسم إشارة مرجعية أو رقم صفحة أو أي عنصر آخر للانتقال إليه في C++."
type: docs
weight: 3000
url: /ar/cpp/aspose.words.fields/fieldgotobutton/get_location/
---
## FieldGoToButton::get_Location method


يحصل أو يضبط اسم إشارة مرجعية أو رقم صفحة أو أي عنصر آخر للقفز إليه.

```cpp
System::String Aspose::Words::Fields::FieldGoToButton::get_Location()
```


## أمثلة



يظهر كيفية إدراج حقل GOTOBUTTON.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// أضف حقل GOTOBUTTON. عندما نقوم بالنقر المزدوج على هذا الحقل في Microsoft Word،
// سوف ينقل مؤشر النص إلى الإشارة المرجعية التي يشير إليها خاصية Location.
auto field = System::ExplicitCast<Aspose::Words::Fields::FieldGoToButton>(builder->InsertField(Aspose::Words::Fields::FieldType::FieldGoToButton, true));
field->set_DisplayText(u"My Button");
field->set_Location(u"MyBookmark");

ASSERT_EQ(u" GOTOBUTTON  MyBookmark My Button", field->GetFieldCode());

// أدرج إشارة مرجعية صالحة ليشير إليها الحقل.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);
builder->StartBookmark(field->get_Location());
builder->Writeln(u"Bookmark text contents.");
builder->EndBookmark(field->get_Location());

doc->UpdateFields();
doc->Save(get_ArtifactsDir() + u"Field.GOTOBUTTON.docx");
```

## انظر أيضًا

* Class [FieldGoToButton](../)
* Namespace [Aspose::Words::Fields](../../)
* Library [Aspose.Words for C++](../../../)
