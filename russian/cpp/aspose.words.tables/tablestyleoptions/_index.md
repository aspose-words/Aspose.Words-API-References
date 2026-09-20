---
title: "Aspose::Words::Tables::TableStyleOptions enum"
linktitle: "TableStyleOptions"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::TableStyleOptions enum. Указывает, как стиль таблицы применяется к таблице в C++."
type: docs
weight: 15000
url: /ru/cpp/aspose.words.tables/tablestyleoptions/
---
## TableStyleOptions enum


Указывает, как стиль таблицы применяется к таблице.

```cpp
enum class TableStyleOptions
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Форматирование стиля таблицы не применяется. |
| FirstRow | 32 | Применить условное форматирование первой строки. |
| LastRow | 64 | Применить условное форматирование последней строки. |
| FirstColumn | 128 | Применить условное форматирование первой колонки 1. |
| LastColumn | 256 | Применить условное форматирование последней колонки. |
| RowBands | 512 | Применить условное форматирование полос строк. |
| ColumnBands | 1024 | Применить условное форматирование полос колонок. |
| Default2003 | n/a | [Row](../row/) и полосы колонок применяются. Это значение по умолчанию Microsoft Word для старых форматов, таких как DOC, WML и RTF. |
| Default | н/д | Это значения по умолчанию Microsoft Word. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
