---
title: "Aspose::Words::ConditionalStyleCollection::get_BottomLeftCell метод"
linktitle: "get_BottomLeftCell"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::ConditionalStyleCollection::get_BottomLeftCell метод. Получает стиль ячейки в нижнем левом углу в C++."
type: docs
weight: 3000
url: /ru/cpp/aspose.words/conditionalstylecollection/get_bottomleftcell/
---
## ConditionalStyleCollection::get_BottomLeftCell method


Возвращает стиль ячейки в нижнем левом углу.

```cpp
System::SharedPtr<Aspose::Words::ConditionalStyle> Aspose::Words::ConditionalStyleCollection::get_BottomLeftCell()
```


## Примеры



Показывает, как работать с некоторыми стилями областей таблицы.
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

// Создайте пользовательский стиль таблицы.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));

// Условные стили — это изменения форматирования, которые влияют только на некоторые ячейки таблицы.
// основанные на предикате, например, ячейки, находящиеся в последней строке.
// Ниже представлены три способа доступа к условным стилям стиля таблицы из коллекции "ConditionalStyles".
// 1 -  По типу стиля:
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::FirstRow)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_AliceBlue());

// 2 -  По индексу:
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_ConditionalStyles()->idx_get(0)->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::DotDash);
ASSERT_EQ(Aspose::Words::ConditionalStyleType::FirstRow, tableStyle->get_ConditionalStyles()->idx_get(0)->get_Type());

// 3 -  Как свойство:
tableStyle->get_ConditionalStyles()->get_FirstRow()->get_ParagraphFormat()->set_Alignment(Aspose::Words::ParagraphAlignment::Center);

// Примените отступы и форматирование текста к условным стилям.
tableStyle->get_ConditionalStyles()->get_LastRow()->set_BottomPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_LeftPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_RightPadding(10);
tableStyle->get_ConditionalStyles()->get_LastRow()->set_TopPadding(10);
tableStyle->get_ConditionalStyles()->get_LastColumn()->get_Font()->set_Bold(true);

// Перечислите все возможные условия стиля.
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

// Примените пользовательский стиль, содержащий все условные стили, к таблице.
table->set_Style(tableStyle);

// Наш стиль применяет некоторые условные стили по умолчанию.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Нам потребуется включить все остальные стили самостоятельно через свойство "StyleOptions".
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::LastRow | Aspose::Words::Tables::TableStyleOptions::LastColumn);

doc->Save(get_ArtifactsDir() + u"Table.ConditionalStyles.docx");
```

## См. также

* Class [ConditionalStyle](../../conditionalstyle/)
* Class [ConditionalStyleCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
