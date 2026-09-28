---
title: "Aspose::Words::ConditionalStyleCollection::ClearFormatting метод"
linktitle: "ClearFormatting"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ConditionalStyleCollection::ClearFormatting метод. Очищает все условные стили табличного стиля в C++."
type: docs
weight: 2000
url: /ru/cpp/aspose.words/conditionalstylecollection/clearformatting/
---
## ConditionalStyleCollection::ClearFormatting method


Очищает все условные стили стиля таблицы.

```cpp
void Aspose::Words::ConditionalStyleCollection::ClearFormatting()
```


## Примеры



Показывает, как сбросить условные стили таблиц.
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

// Установите стиль таблицы, чтобы окрасить границы первой строки таблицы в красный цвет.
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->set_Color(System::Drawing::Color::get_Red());

// Установите стиль таблицы, чтобы окрасить границы последней строки таблицы в синий цвет.
tableStyle->get_ConditionalStyles()->get_LastRow()->get_Borders()->set_Color(System::Drawing::Color::get_Blue());

// Ниже представлены два способа использования метода "ClearFormatting" для очистки условных стилей.
// 1 -  Очистить условные стили для определённой части таблицы:
tableStyle->get_ConditionalStyles()->idx_get(0)->ClearFormatting();

ASPOSE_ASSERT_EQ(System::Drawing::Color::Empty, tableStyle->get_ConditionalStyles()->get_FirstRow()->get_Borders()->get_Color());

// 2 -  Очистить условные стили для всей таблицы:
tableStyle->get_ConditionalStyles()->ClearFormatting();

ASSERT_TRUE(tableStyle->get_ConditionalStyles()->LINQ_All(static_cast<System::Func<System::SharedPtr<Aspose::Words::ConditionalStyle>, bool>>(static_cast<std::function<bool(System::SharedPtr<Aspose::Words::ConditionalStyle> s)>>([](System::SharedPtr<Aspose::Words::ConditionalStyle> s) -> bool
{
    return s->get_Borders()->get_Color() == System::Drawing::Color::Empty;
}))));
```

## См. также

* Class [ConditionalStyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
