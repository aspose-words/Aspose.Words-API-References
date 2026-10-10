---
title: "Aspose::Words::Tables::Table::get_TextWrapping طريقة"
linktitle: "get_TextWrapping"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::Table::get_TextWrapping طريقة. يحصل أو يحدد TextWrapping للجدول في C++."
type: docs
weight: 38000
url: /ar/cpp/aspose.words.tables/table/get_textwrapping/
---
## Table::get_TextWrapping method


يحصل أو يحدد [TextWrapping](./) للجدول.

```cpp
Aspose::Words::Tables::TextWrapping Aspose::Words::Tables::Table::get_TextWrapping()
```


## أمثلة



يظهر كيفية العمل مع لف النص حول الجدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

builder->get_Font()->set_Size(16);
builder->Writeln(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// قم بتعيين الخاصية "TextWrapping" إلى "TextWrapping.Around" لجعل الجدول يلف النص حوله،
// وإسحابه للأسفل إلى الفقرة أدناه عن طريق ضبط الموضع.
table->set_TextWrapping(Aspose::Words::Tables::TextWrapping::Around);
table->set_AbsoluteHorizontalDistance(100);
table->set_AbsoluteVerticalDistance(20);

doc->Save(get_ArtifactsDir() + u"Table.WrapText.docx");
```

## انظر أيضًا

* Enum [TextWrapping](../../textwrapping/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
