---
title: "Aspose::Words::Tables::TextWrapping enum"
linktitle: "TextWrapping"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::Tables::TextWrapping enum. يحدد كيفية التفاف النص حول الجدول في C++."
type: docs
weight: 16000
url: /ar/cpp/aspose.words.tables/textwrapping/
---
## TextWrapping enum


يحدد كيفية التفاف النص حول الجدول.

```cpp
enum class TextWrapping
```

### القيم

| الاسم | القيمة | الوصف |
| --- | --- | --- |
| None | 0 | يتم عرض النص والجدول بترتيب ظهورهما في المستند. |
| حول | 1 | يتم لف النص حول الجدول مشغولًا المساحة الجانبية المتاحة. |
| افتراضي | n/a | القيمة الافتراضية. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
