---
title: "Метод Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance"
linktitle: "get_AbsoluteHorizontalDistance"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance. Получает или задает абсолютную горизонтальную позицию плавающей таблицы, указанную в свойствах таблицы, в пунктах. Значение по умолчанию — 0 в C++."
type: docs
weight: 9000
url: /ru/cpp/aspose.words.tables/table/get_absolutehorizontaldistance/
---
## Table::get_AbsoluteHorizontalDistance method


Получает или задаёт абсолютную горизонтальную позицию плавающей таблицы, указанную в свойствах таблицы, в пунктах. Значение по умолчанию — 0.

```cpp
double Aspose::Words::Tables::Table::get_AbsoluteHorizontalDistance()
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
