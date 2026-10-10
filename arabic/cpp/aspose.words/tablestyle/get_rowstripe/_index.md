---
title: "طريقة Aspose::Words::TableStyle::get_RowStripe"
linktitle: "get_RowStripe"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "طريقة Aspose::Words::TableStyle::get_RowStripe. يحصل أو يحدد عدد الصفوف التي يجب تضمينها في النطاق عندما يحدد النمط تظليل الصفوف الفردية/الزوجية في C++."
type: docs
weight: 13000
url: /ar/cpp/aspose.words/tablestyle/get_rowstripe/
---
## TableStyle::get_RowStripe method


يحصل أو يضبط عدد الصفوف التي تُضمّن في التظليل عندما يحدد النمط تظليل الصفوف الفردية/الزوجية.

```cpp
int32_t Aspose::Words::TableStyle::get_RowStripe()
```


## أمثلة



يوضح كيفية إنشاء أنماط جدول شرطية تتناوب بين الصفوف.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// يمكننا تكوين نمط شرطي للجدول لتطبيق لون مختلف على الصف/العمود،
// استنادًا إلى ما إذا كان الصف/العمود زوجيًا أو فرديًا، مما يخلق نمط لون متناوب.
// يمكننا أيضًا تطبيق رقم n على تظليل الصف/العمود،
// مما يعني أن اللون يتناوب بعد كل n صفوف/أعمدة بدلاً من واحد.
// إنشاء جدول حيث سيتم تظليل الأعمدة والصفوف المفردة بحيث تُظلل الأعمدة على مجموعات من ثلاثة.
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
for (int32_t i = 0; i < 15; i++)
{
    for (int32_t j = 0; j < 4; j++)
    {
        builder->InsertCell();
        builder->Writeln(System::String::Format(u"{0} column.", (j % 2 == 0 ? System::String(u"Even") : System::String(u"Odd"))));
        builder->Write(System::String::Format(u"Row banding {0}.", (i % 3 == 0 ? System::String(u"start") : System::String(u"continuation"))));
    }
    builder->EndRow();
}
builder->EndTable();

// تطبيق نمط خط على جميع حدود الجدول.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);

// تعيين اللونين، اللذين سيتناوبان كل 3 صفوف.
tableStyle->set_RowStripe(3);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::OddRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightCyan());

// تعيين لون لتطبيقه على كل عمود زوجي، والذي سيتجاوز أي تلوين مخصص للصفوف.
tableStyle->set_ColumnStripe(1);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenColumnBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSalmon());

table->set_Style(tableStyle);

// خاصية "StyleOptions" تمكّن تظليل الصفوف بشكل افتراضي.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// استخدم خاصية "StyleOptions" أيضًا لتمكين تظليل الأعمدة.
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::ColumnBands);

doc->Save(get_ArtifactsDir() + u"Table.AlternatingRowStyles.docx");
```

## انظر أيضًا

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
