---
title: "Aspose::Words::Tables::Table::get_StyleIdentifier метод"
linktitle: "get_StyleIdentifier"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::get_StyleIdentifier метод. Получает или задает независимый от локали идентификатор стиля таблицы, применяемый к этой таблице в C++."
type: docs
weight: 35000
url: /ru/cpp/aspose.words.tables/table/get_styleidentifier/
---
## Table::get_StyleIdentifier method


Получает или задает независимый от локали идентификатор стиля таблицы, применяемый к этой таблице.

```cpp
Aspose::Words::StyleIdentifier Aspose::Words::Tables::Table::get_StyleIdentifier()
```


## Примеры



Показывает, как создать новую таблицу, применяя стиль.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();

// Мы должны вставить как минимум одну строку перед применением любого форматирования таблицы.
builder->InsertCell();

// Установите стиль таблицы, используемый на основе идентификатора стиля.
// Обратите внимание, что не все стили таблиц доступны при сохранении в формат .doc.
table->set_StyleIdentifier(Aspose::Words::StyleIdentifier::MediumShading1Accent1);

// Частично примените стиль к элементам таблицы на основе предикатов, затем постройте таблицу.
table->set_StyleOptions(Aspose::Words::Tables::TableStyleOptions::FirstColumn | Aspose::Words::Tables::TableStyleOptions::RowBands | Aspose::Words::Tables::TableStyleOptions::FirstRow);
table->AutoFit(Aspose::Words::Tables::AutoFitBehavior::AutoFitToContents);

builder->Writeln(u"Item");
builder->get_CellFormat()->set_RightPadding(40);
builder->InsertCell();
builder->Writeln(u"Quantity (kg)");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Apples");
builder->InsertCell();
builder->Writeln(u"20");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Bananas");
builder->InsertCell();
builder->Writeln(u"40");
builder->EndRow();

builder->InsertCell();
builder->Writeln(u"Carrots");
builder->InsertCell();
builder->Writeln(u"50");
builder->EndRow();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertTableWithStyle.docx");
```

## См. также

* Enum [StyleIdentifier](../../../aspose.words/styleidentifier/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
