---
title: "Aspose::Words::DocumentBuilder::InsertCell method"
linktitle: "InsertCell"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::DocumentBuilder::InsertCell method. يُدرج خلية جدول في المستند في C++."
type: docs
weight: 29000
url: /ar/cpp/aspose.words/documentbuilder/insertcell/
---
## DocumentBuilder::InsertCell method


يدرج خلية جدول في المستند.

```cpp
System::SharedPtr<Aspose::Words::Tables::Cell> Aspose::Words::DocumentBuilder::InsertCell()
```


### ReturnValue

عقدة الخلية التي تم إدراجها للتو.
## ملاحظات


لبدء جدول، ما عليك سوى استدعاء [InsertCell](./). بعد ذلك، سيتم إضافة أي محتوى تضيفه باستخدام طرق أخرى من فئة [DocumentBuilder](../) إلى الخلية الحالية.

لبدء خلية جديدة في نفس الصف، استدعِ [InsertCell](./) مرة أخرى.

لإنهاء صف جدول استدعِ [EndRow](../endrow/).

استخدم خاصية [CellFormat](../get_cellformat/) لتحديد تنسيق الخلية.

## أمثلة



يوضح كيفية بناء جدول بحدود مخصصة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

builder->StartTable();

// تعيين خيارات تنسيق الجدول لمنشئ المستند
// سيتم تطبيقها على كل صف وخلية نضيفها به.
builder->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

builder->get_CellFormat()->ClearFormatting();
builder->get_CellFormat()->set_Width(150);
builder->get_CellFormat()->set_VerticalAlignment(Aspose::Words::Tables::CellVerticalAlignment::Center);
builder->get_CellFormat()->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_GreenYellow());
builder->get_CellFormat()->set_WrapText(false);
builder->get_CellFormat()->set_FitText(true);

builder->get_RowFormat()->ClearFormatting();
builder->get_RowFormat()->set_HeightRule(Aspose::Words::HeightRule::Exactly);
builder->get_RowFormat()->set_Height(50);
builder->get_RowFormat()->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Engrave3D);
builder->get_RowFormat()->get_Borders()->set_Color(System::Drawing::Color::get_Orange());

builder->InsertCell();
builder->Write(u"Row 1, Col 1");

builder->InsertCell();
builder->Write(u"Row 1, Col 2");
builder->EndRow();

// تغيير التنسيق سيطبقه على الخلية الحالية،
// وأي خلايا جديدة ننشئها باستخدام المنشئ لاحقًا.
// هذا لن يؤثر على الخلايا التي أضفناها مسبقًا.
builder->get_CellFormat()->get_Shading()->ClearFormatting();

builder->InsertCell();
builder->Write(u"Row 2, Col 1");

builder->InsertCell();
builder->Write(u"Row 2, Col 2");

builder->EndRow();

// زد ارتفاع الصف لتناسب النص العمودي.
builder->InsertCell();
builder->get_RowFormat()->set_Height(150);
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Upward);
builder->Write(u"Row 3, Col 1");

builder->InsertCell();
builder->get_CellFormat()->set_Orientation(Aspose::Words::TextOrientation::Downward);
builder->Write(u"Row 3, Col 2");

builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTable.docx");
```


يوضح كيفية استخدام منشئ المستند لإنشاء جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// ابدأ الجدول، ثم املأ الصف الأول بخليةين.
builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, Cell 2.");

// استدعِ طريقة "EndRow" للمنشئ لبدء صف جديد.
builder->EndRow();
builder->InsertCell();
builder->Write(u"Row 2, Cell 1.");
builder->InsertCell();
builder->Write(u"Row 2, Cell 2.");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.CreateTable.docx");
```

## انظر أيضًا

* Class [Cell](../../../aspose.words.tables/cell/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
