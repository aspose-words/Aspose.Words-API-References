---
title: "Aspose::Words::ConditionalStyleCollection::ClearFormatting طريقة"
linktitle: "ClearFormatting"
second_title: "مرجع API لـ Aspose.Words للغة C++"
description: "Aspose::Words::ConditionalStyleCollection::ClearFormatting طريقة. يمسح جميع الأنماط الشرطية لنمط الجدول في C++."
type: docs
weight: 2000
url: /ar/cpp/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection::ClearFormatting method


يمسح جميع الأنماط الشرطية لنمط الجدول.

```cpp
void Aspose::Words::ConditionalStyleCollection::ClearFormatting()
```


## أمثلة



يظهر كيفية إعادة ضبط أنماط الجداول الشرطية.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"First row");
builder->EndRow();
builder->InsertCell();
builder->Write(u"Last row");
builder->EndTable();

auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
table->set_Style(tableStyle);

// قم بتعيين نمط الجدول لتلوين حدود الصف الأول من الجدول باللون الأحمر.
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->set_Color(System::Drawing::Color::get_Red());

// قم بتعيين نمط الجدول لتلوين حدود الصف الأخير من الجدول باللون الأزرق.
tableStyle->get_ConditionalStyles()->get_LastRow()->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// فيما يلي طريقتان لاستخدام طريقة "ClearFormatting" لمسح الأنماط الشرطية.
// 1 -  مسح الأنماط الشرطية لجزء محدد من جدول:
tableStyle->get_ConditionalStyles()->idx_get(0)->ClearFormatting();

ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->get_Color());

// 2 -  مسح الأنماط الشرطية للجدول بأكمله:
tableStyle->get_ConditionalStyles()->ClearFormatting();

ASSERT_TRUE(tableStyle->get_ConditionalStyles()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::ConditionalStyle>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::ConditionalStyle> s)>>([](System::SharedPtr<Aspose::Words::ConditionalStyle> s) -> bool
{
    return s->get_Borders()->get_Color() == System::Drawing::Color::Empty;
}))));
```

## انظر أيضًا

* Class [ConditionalStyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
