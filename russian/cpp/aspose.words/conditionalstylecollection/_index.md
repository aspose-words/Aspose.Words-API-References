---
title: "Класс Aspose::Words::ConditionalStyleCollection"
linktitle: "ConditionalStyleCollection"
second_title: "Справочник API Aspose.Words для C++"
description: "Класс Aspose::Words::ConditionalStyleCollection. Представляет коллекцию объектов ConditionalStyle. Чтобы узнать больше, посетите статью документации на C++."
type: docs
weight: 17000
url: /ru/cpp/aspose.words/conditionalstylecollection/
---
## ConditionalStyleCollection class


Представляет коллекцию объектов [ConditionalStyle](../conditionalstyle/). Чтобы узнать больше, посетите статью документации [Working with Tables](https://docs.aspose.com/words/cpp/working-with-tables/).

```cpp
class ConditionalStyleCollection : public System::Collections::Generic::IEnumerable<System::SharedPtr<Aspose::Words::ConditionalStyle>>
```

## Методы

| Метод | Описание |
| --- | --- |
| [ClearFormatting](./clearformatting/)() | Очищает все условные стили стиля таблицы. |
| [get_BottomLeftCell](./get_bottomleftcell/)() | Возвращает стиль ячейки в нижнем левом углу. |
| [get_BottomRightCell](./get_bottomrightcell/)() | Возвращает стиль ячейки в нижнем правом углу. |
| [get_Count](./get_count/)() const | Возвращает количество условных стилей в коллекции. |
| [get_EvenColumnBanding](./get_evencolumnbanding/)() | Возвращает стиль чередования четных столбцов. |
| [get_EvenRowBanding](./get_evenrowbanding/)() | Получает стиль чередования чётных строк. |
| [get_FirstColumn](./get_firstcolumn/)() | Получает стиль первого столбца. |
| [get_FirstRow](./get_firstrow/)() | Получает стиль первой строки. |
| [get_LastColumn](./get_lastcolumn/)() | Получает стиль последнего столбца. |
| [get_LastRow](./get_lastrow/)() | Получает стиль последней строки. |
| [get_OddColumnBanding](./get_oddcolumnbanding/)() | Получает стиль чередования нечётных столбцов. |
| [get_OddRowBanding](./get_oddrowbanding/)() | Получает стиль чередования нечётных строк. |
| [get_TopLeftCell](./get_topleftcell/)() | Получает стиль ячейки в левом верхнем углу. |
| [get_TopRightCell](./get_toprightcell/)() | Получает стиль ячейки в правом верхнем углу. |
| [GetEnumerator](./getenumerator/)() override | Возвращает объект‑перечислитель, который можно использовать для перебора всех условных стилей в коллекции. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(Aspose::Words::ConditionalStyleType) | Получает объект [ConditionalStyle](../conditionalstyle/) по типу условного стиля. |
| [idx_get](./idx_get/)(int32_t) | Получает объект [ConditionalStyle](../conditionalstyle/) по индексу. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
