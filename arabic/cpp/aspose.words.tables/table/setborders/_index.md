---
title: "طريقة Aspose::Words::Tables::Table::SetBorders"
linktitle: "SetBorders"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::Tables::Table::SetBorders. تُعيّن جميع حدود الجدول إلى نمط الخط المحدد والعرض واللون في C++."
type: docs
weight: 69000
url: /ar/cpp/aspose.words.tables/table/setborders/
---
## Table::SetBorders method


يضبط جميع حدود الجدول إلى نمط الخط والعرض واللون المحددين.

```cpp
void Aspose::Words::Tables::Table::SetBorders(Aspose::Words::LineStyle lineStyle, double lineWidth, System::Drawing::Color color)
```


| معامل | النوع | الوصف |
| --- | --- | --- |
| lineStyle | Aspose::Words::LineStyle | نمط الخط المراد تطبيقه. |
| lineWidth | double | عرض الخط المراد ضبطه (بالنقاط). |
| color | System::Drawing::Color | اللون المراد استخدامه للحد. |

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


يظهر كيفية تنسيق جميع حدود الجدول مرة واحدة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Tables.docx");
System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);

// امسح جميع الحدود الموجودة من الجدول.
table->ClearBorders();

// عيّن خطًا أخضر واحدًا ليكون كل حد خارجي وداخلي لهذا الجدول.
table->SetBorders(Aspose::Words::LineStyle::Single, 1.5, System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Table.SetBorders.docx");
```

## انظر أيضًا

* Enum [LineStyle](../../../aspose.words/linestyle/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
