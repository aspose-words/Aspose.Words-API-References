---
title: "Aspose::Words::Tables::Table::get_BottomPadding метод"
linktitle: "get_BottomPadding"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::get_BottomPadding метод. Получает или задает количество пространства (в пунктах), добавляемого под содержимое ячеек в C++."
type: docs
weight: 16000
url: /ru/cpp/aspose.words.tables/table/get_bottompadding/
---
## Table::get_BottomPadding method


Получает или задаёт количество пространства (в пунктах), добавляемого под содержимое ячеек.

```cpp
double Aspose::Words::Tables::Table::get_BottomPadding()
```


## Примеры



Показывает, как настроить отступ содержимого в таблице.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Row 1, cell 1.");
builder->InsertCell();
builder->Write(u"Row 1, cell 2.");
builder->EndTable();

// Для каждой ячейки в таблице задайте расстояние между её содержимым и каждой из её границ.
// Эта таблица будет поддерживать минимальное расстояние отступа, оборачивая текст.
table->set_LeftPadding(30);
table->set_RightPadding(60);
table->set_TopPadding(10);
table->set_BottomPadding(90);
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(250));

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.SetRowFormatting.docx");
```

## См. также

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
