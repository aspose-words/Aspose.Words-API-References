---
title: "Aspose::Words::BorderCollection::get_Bottom method"
linktitle: "get_Bottom"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::BorderCollection::get_Bottom method. يحصل على الحد السفلي في C++."
type: docs
weight: 4000
url: /ar/cpp/aspose.words/bordercollection/get_bottom/
---
## BorderCollection::get_Bottom method


يحصل على الحد السفلي.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Bottom()
```


## أمثلة



يوضح كيفية تطبيق لون الحدود والتظليل أثناء بناء جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// ابدأ جدولًا وحدد لونًا/سماكةً افتراضيةً لحدوده.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
table->SetBorders(Aspose::Words::LineStyle::Single, 2.0, System::Drawing::Color::get_Black());

// أنشئ صفًا يحتوي على خليتين بألوان خلفية مختلفة.
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSkyBlue());
builder->Writeln(u"Row 1, Cell 1.");
builder->InsertCell();
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_Orange());
builder->Writeln(u"Row 1, Cell 2.");
builder->EndRow();

// إعادة تعيين تنسيق الخلية لتعطيل ألوان الخلفية
// حدد سماكة حد مخصصة لجميع الخلايا الجديدة التي ينشئها المُنشئ،
// ثم أنشئ صفًا ثانيًا.
builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->get_Borders()->get_Left()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Right()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Top()->set_LineWidth(4.0);
builder->get_CellFormat()->get_Borders()->get_Bottom()->set_LineWidth(4.0);

builder->InsertCell();
builder->Writeln(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Writeln(u"Row 2, Cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.TableBordersAndShading.docx");
```

## انظر أيضًا

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
