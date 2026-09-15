---
title: "طريقة Aspose::Words::BorderCollection::get_Horizontal"
linktitle: "get_Horizontal"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::BorderCollection::get_Horizontal. يحصل على الحد الأفقي المستخدم بين الخلايا أو الفقرات المتطابقة في C++."
type: docs
weight: 8000
url: /ar/cpp/aspose.words/bordercollection/get_horizontal/
---
## BorderCollection::get_Horizontal method


يحصل على الحد الأفقي المستخدم بين الخلايا أو الفقرات المتوافقة.

```cpp
System::SharedPtr<Aspose::Words::Border> Aspose::Words::BorderCollection::get_Horizontal()
```


## أمثلة



يوضح كيفية تطبيق الإعدادات على الحدود الأفقية لتنسيق الفقرة.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء حد أفقي أحمر للفقرة. أي فقرات تُنشأ لاحقًا ستورث إعدادات هذا الحد.
System::SharedPtr<Aspose::Words::BorderCollection> borders = doc->get_FirstSection()->get_Body()->get_FirstParagraph()->get_ParagraphFormat()->get_Borders();
borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::DashSmallGap);
borders->get_Horizontal()->set_LineWidth(3);

// اكتب نصًا إلى المستند دون إنشاء فقرة جديدة بعد ذلك.
// نظرًا لعدم وجود فقرة أسفلها، لن يكون الحد الأفقي مرئيًا.
builder->Write(u"Paragraph above horizontal border.");

// بمجرد إضافة فقرة ثانية، سيصبح حد الفقرة الأولى مرئيًا.
builder->InsertParagraph();
builder->Write(u"Paragraph below horizontal border.");

doc->Save(get_ArtifactsDir() + u"Border.HorizontalBorders.docx");
```


يوضح كيفية تطبيق الإعدادات على الحدود العمودية لتنسيق صف الجدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// إنشاء جدول بحدود داخلية حمراء وزرقاء.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

for (int32_t i = 0; i < 3; i++)
{
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 1", i + 1));
    builder->InsertCell();
    builder->Write(System::String::Format(u"Row {0}, Column 2", i + 1));

    System::SharedPtr<Aspose::Words::Tables::Row> row = builder->EndRow();
    System::SharedPtr<Aspose::Words::BorderCollection> borders = row->get_RowFormat()->get_Borders();

    // ضبط مظهر الحدود التي ستظهر بين الصفوف.
    borders->get_Horizontal()->set_Color(System::Drawing::Color::get_Red());
    borders->get_Horizontal()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Horizontal()->set_LineWidth(2.0);

    // ضبط مظهر الحدود التي ستظهر بين الخلايا.
    borders->get_Vertical()->set_Color(System::Drawing::Color::get_Blue());
    borders->get_Vertical()->set_LineStyle(Aspose::Words::LineStyle::Dot);
    borders->get_Vertical()->set_LineWidth(2.0);
}

// تنسيق الصف، وفقرة الخلية الداخلية تستخدم إعدادات حدود مختلفة.
System::SharedPtr<Aspose::Words::Border> border = table->get_FirstRow()->get_FirstCell()->get_LastParagraph()->get_ParagraphFormat()->get_Borders()->get_Vertical();

ASSERT_EQ(System::Drawing::Color::Empty.ToArgb(), border->get_Color().ToArgb());
ASPOSE_ASSERT_EQ(0.0, border->get_LineWidth());
ASSERT_EQ(Aspose::Words::LineStyle::None, border->get_LineStyle());

doc->Save(get_ArtifactsDir() + u"Border.VerticalBorders.docx");
```

## انظر أيضًا

* Class [Border](../../border/)
* Class [BorderCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
