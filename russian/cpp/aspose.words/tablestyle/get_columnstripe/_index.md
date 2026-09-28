---
title: "Aspose::Words::TableStyle::get_ColumnStripe метод"
linktitle: "get_ColumnStripe"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::TableStyle::get_ColumnStripe метод. Получает или задаёт количество столбцов, включаемых в полосатость, когда стиль указывает полосатость нечётных/чётных столбцов в C++."
type: docs
weight: 8000
url: /ru/cpp/aspose.words/tablestyle/get_columnstripe/
---
## TableStyle::get_ColumnStripe method


Получает или задает количество столбцов, включаемых в чередование, когда стиль указывает чередование нечётных/чётных столбцов.

```cpp
int32_t Aspose::Words::TableStyle::get_ColumnStripe()
```


## Примеры



Показывает, как создавать условные стили таблиц, чередующиеся между строками.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Мы можем настроить условный стиль таблицы, чтобы применять другой цвет к строке/столбцу,
// исходя из того, является ли строка/столбец чётным или нечётным, создавая чередующийся цветовой шаблон.
// Мы также можем задать число n для полосатости строк/столбцов,
// что означает, что цвет меняется после каждых n строк/столбцов вместо одной.
// Создайте таблицу, где отдельные столбцы и строки будут полосатыми, а столбцы будут сгруппированы по три.
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

// Примените линейный стиль ко всем границам таблицы.
auto tableStyle = System::ExplicitCast<Aspose::Words::TableStyle>(doc->get_Styles()->Add(Aspose::Words::StyleType::Table, u"MyTableStyle1"));
tableStyle->get_Borders()->set_Color(System::Drawing::Color::get_Black());
tableStyle->get_Borders()->set_LineStyle(Aspose::Words::LineStyle::Double);

// Установите два цвета, которые будут чередоваться каждые 3 строки.
tableStyle->set_RowStripe(3);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::OddRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightBlue());
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenRowBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightCyan());

// Установите цвет, применяемый к каждому чётному столбцу, который переопределит любую пользовательскую раскраску строк.
tableStyle->set_ColumnStripe(1);
tableStyle->get_ConditionalStyles()->idx_get(Aspose::Words::ConditionalStyleType::EvenColumnBanding)->get_Shading()->set_BackgroundPatternColor(System::Drawing::Color::get_LightSalmon());

table->set_Style(tableStyle);

// Свойство "StyleOptions" включает полосатость строк по умолчанию.
ASSERT_EQ(Aspose::Words::Tables::TableStyleOptions::FirstRow | Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands, table->get_StyleOptions());

// Также используйте свойство "StyleOptions" для включения полосатости столбцов.
table->set_StyleOptions(table->get_StyleOptions() | Aspose::Words::Tables::TableStyleOptions::ColumnBands);

doc->Save(get_ArtifactsDir() + u"Table.AlternatingRowStyles.docx");
```

## См. также

* Class [TableStyle](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
