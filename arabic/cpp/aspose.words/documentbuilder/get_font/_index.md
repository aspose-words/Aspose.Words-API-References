---
title: "طريقة Aspose::Words::DocumentBuilder::get_Font"
linktitle: "get_Font"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::DocumentBuilder::get_Font. تُرجع كائنًا يمثل خصائص تنسيق الخط الحالي في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words/documentbuilder/get_font/
---
## DocumentBuilder::get_Font method


يرجع كائنًا يمثل خصائص تنسيق الخط الحالية.

```cpp
System::SharedPtr<Aspose::Words::Font> Aspose::Words::DocumentBuilder::get_Font()
```

## ملاحظات


استخدم [Font](./) للوصول إلى خصائص تنسيق الخط وتعديلها.

حدد تنسيق الخط قبل إدراج النص.

## أمثلة



يوضح كيفية إدراج سلسلة محاطة بحد داخل مستند.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->get_Font()->get_Border()->set_Color(System::Drawing::Color::get_Green());
builder->get_Font()->get_Border()->set_LineWidth(2.5);
builder->get_Font()->get_Border()->set_LineStyle(Aspose::Words::LineStyle::DashDotStroker);

builder->Write(u"Text surrounded by green border.");

doc->Save(get_ArtifactsDir() + u"Border.FontBorder.docx");
```


يظهر كيفية إنشاء جدول منسق باستخدام [DocumentBuilder](../).
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
table->set_LeftIndent(20);

// قم بتعيين بعض خيارات التنسيق للنص ومظهر الجدول.
builder->get_RowFormat()->set_Height(40);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::AtLeast);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::FromArgb(198, 217, 241));

builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);
builder->get_Font()->set_Size(16);
builder->get_Font()->set_Name(u"Arial");
builder->get_Font()->set_Bold(true);

// سيؤدي تكوين خيارات التنسيق في مُنشئ المستند إلى تطبيقها
// على الخلية/الصف الحالي الذي يوجد فيه المؤشر،
// وكذلك أي خلايا وصفوف جديدة تم إنشاؤها باستخدام ذلك المُنشئ.
builder->Write(u"Header Row,\n Cell 1");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 2");
builder->InsertCell();
builder->Write(u"Header Row,\n Cell 3");
builder->EndRow();

// أعد تكوين كائنات تنسيق المُنشئ للصفوف والخلايا الجديدة التي نحن على وشك إنشائها.
// لن يطبق المُنشئ هذه على الصف الأول الذي تم إنشاؤه بالفعل حتى يبرز كصف رأس.
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_White());
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_RowFormat()->set_Height(30);
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Auto);
builder->InsertCell();
builder->get_Font()->set_Size(12);
builder->get_Font()->set_Bold(false);

builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 3.");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 3.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateFormattedTable.docx");
```

## انظر أيضًا

* Class [Font](../../font/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
