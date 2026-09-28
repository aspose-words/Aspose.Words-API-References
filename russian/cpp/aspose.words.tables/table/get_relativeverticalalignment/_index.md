---
title: "Aspose::Words::Tables::Table::get_RelativeVerticalAlignment метод"
linktitle: "get_RelativeVerticalAlignment"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::get_RelativeVerticalAlignment метод. Получает или задает относительное вертикальное выравнивание плавающей таблицы в C++."
type: docs
weight: 31000
url: /ru/cpp/aspose.words.tables/table/get_relativeverticalalignment/
---
## Table::get_RelativeVerticalAlignment method


Получает или задает относительное вертикальное выравнивание плавающей таблицы.

```cpp
Aspose::Words::Drawing::VerticalAlignment Aspose::Words::Tables::Table::get_RelativeVerticalAlignment()
```


## Примеры



Показывает, как установить расположение плавающих таблиц.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::Tables::Table> table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 1, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Установите расположение таблицы в определённое место на странице, например, в данном случае — в правый нижний угол.
table->set_RelativeVerticalAlignment(Aspose::Words::Drawing::VerticalAlignment::Bottom);
table->set_RelativeHorizontalAlignment(Aspose::Words::Drawing::HorizontalAlignment::Right);

table = builder->StartTable();
builder->InsertCell();
builder->Write(u"Table 2, cell 1");
builder->EndTable();
table->set_PreferredWidth(Aspose::Words::Tables::PreferredWidth::FromPoints(300));

// Мы также можем задать горизонтальное и вертикальное смещение в пунктах от положения абзаца, где была вставлена таблица.
table->set_AbsoluteVerticalDistance(50);
table->set_AbsoluteHorizontalDistance(100);

doc->Save(get_ArtifactsDir() + u"Table.ChangeFloatingTableProperties.docx");
```

## См. также

* Enum [VerticalAlignment](../../../aspose.words.drawing/verticalalignment/)
* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
