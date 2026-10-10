---
title: "فئة Aspose::Words::ConditionalStyleCollection"
linktitle: "ConditionalStyleCollection"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "فئة Aspose::Words::ConditionalStyleCollection. تمثل مجموعة من كائنات ConditionalStyle. لمعرفة المزيد، زر مقالة الوثائق في C++."
type: docs
weight: 17000
url: /ar/cpp/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class


تمثل مجموعة من كائنات [ConditionalStyle](../conditionalstyle/). لمعرفة المزيد، زر مقالة الوثائق [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::ConditionalStyle>>
```

## الطرق

| طريقة | الوصف |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | يمسح جميع الأنماط الشرطية لنمط الجدول. |
| [get_BottomLeftCell](./get_bottomleftcell/)() | يحصل على نمط الخلية السفلية اليسرى. |
| [get_BottomRightCell](./get_bottomrightcell/)() | يحصل على نمط الخلية السفلية اليمنى. |
| [get_Count](./get_count/)() const | يحصل على عدد الأنماط الشرطية في المجموعة. |
| [get_EvenColumnBanding](./get_evencolumnbanding/)() | يحصل على نمط تظليل الأعمدة الزوجية. |
| [get_EvenRowBanding](./get_evenrowbanding/)() | يحصل على نمط تظليل الصفوف الزوجية. |
| [get_FirstColumn](./get_firstcolumn/)() | يحصل على نمط العمود الأول. |
| [get_FirstRow](./get_firstrow/)() | يحصل على نمط الصف الأول. |
| [get_LastColumn](./get_lastcolumn/)() | يحصل على نمط العمود الأخير. |
| [get_LastRow](./get_lastrow/)() | يحصل على نمط الصف الأخير. |
| [get_OddColumnBanding](./get_oddcolumnbanding/)() | يحصل على نمط تظليل العمود الفردي. |
| [get_OddRowBanding](./get_oddrowbanding/)() | يحصل على نمط تظليل الصف الفردي. |
| [get_TopLeftCell](./get_topleftcell/)() | يحصل على نمط الخلية العليا اليسرى. |
| [get_TopRightCell](./get_toprightcell/)() | يحصل على نمط الخلية العليا اليمنى. |
| [GetEnumerator](./getenumerator/)() override | يعيد كائن عداد يمكن استخدامه للتكرار عبر جميع الأنماط الشرطية في المجموعة. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::ConditionalStyleType) | يسترجع كائن [ConditionalStyle](../conditionalstyle/) حسب نوع النمط الشرطي. |
| [idx_get](./idx_get/)(int32_t) | يسترجع كائن [ConditionalStyle](../conditionalstyle/) حسب الفهرس. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

## أمثلة



يظهر كيفية العمل مع أنماط مناطق معينة في جدول.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Cell 1");
builder->InsertCell();
builder->Write(u"Cell 2");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Cell 3");
builder->InsertCell();
builder->Write(u"Cell 4");
builder->EndTable();

// إنشاء نمط جدول مخصص.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));

// الأنماط الشرطية هي تغييرات تنسيق تؤثر فقط على بعض خلايا الجدول.
// استنادًا إلى شرط، مثل كون الخلايا في الصف الأخير.
// فيما يلي ثلاث طرق للوصول إلى الأنماط الشرطية لنمط جدول من مجموعة "ConditionalStyles".
// 1 -  حسب نوع النمط:
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::FirstRow)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AliceBlue());

// 2 -  حسب الفهرس:
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
ASSERT_EQ(Aspose::Words::ConditionalStyleType::FirstRow, tableStyle->get_ConditionalStyles()->idx_get(0)->get_Type());

// 3 -  كخاصية:
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// تطبيق الحشو وتنسيق النص على الأنماط الشرطية.
tableStyle->get_ConditionalStyles()->get_LastRow()->set_BottomPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_LeftPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_RightPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_TopPadding(10);
tableStyle->get_ConditionalStyles()->get_LastColumn()->get_Font()->set_Bold(true);

// قائمة بجميع شروط النمط الممكنة.
{
    System::SharedPtr<System::Collections::Generic::IEnumerator<System::SharedPtr<Aspose::Words::ConditionalStyle>>> enumerator = tableStyle->get_ConditionalStyles()->GetEnumerator();
    while (enumerator->MoveNext())
    {
        System::SharedPtr<Aspose::Words::ConditionalStyle> currentStyle = enumerator->get_Current();
        if (currentStyle != nullptr)
        {
            std::cout << System::EnumGetName(currentStyle->get_Type()) << std::endl;
        }
    }
}

// تطبيق النمط المخصص، الذي يحتوي على جميع الأنماط الشرطية، على الجدول.
table->set_Style(tableStyle);

// نمطنا يطبق بعض الأنماط الشرطية بشكل افتراضي.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// سنحتاج إلى تمكين جميع الأنماط الأخرى بأنفسنا عبر خاصية "StyleOptions".
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::LastRow | Aspose::Words::Tables::TableStyleOptions::LastColumn);

doc->Save(get_ArtifactsDir() + u"Table.ConditionalStyles.docx");
```

## انظر أيضًا

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
