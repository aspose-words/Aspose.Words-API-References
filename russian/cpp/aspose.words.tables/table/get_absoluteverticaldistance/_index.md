---
title: "Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance метод"
linktitle: "get_AbsoluteVerticalDistance"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance метод. Получает или задает абсолютную вертикальную позицию плавающей таблицы, указанную в свойствах таблицы, в пунктах. Значение по умолчанию — 0 в C++."
type: docs
weight: 10000
url: /ru/cpp/aspose.words.tables/table/get_absoluteverticaldistance/
---
## Table::get_AbsoluteVerticalDistance method


Получает или задаёт абсолютную вертикальную позицию плавающей таблицы, указанную в свойствах таблицы, в пунктах. Значение по умолчанию — 0.

```cpp
double Aspose::Words::Tables::Table::get_AbsoluteVerticalDistance()
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

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
