---
title: "Aspose::Words::Tables::Table::get_DistanceBottom метод"
linktitle: "get_DistanceBottom"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Table::get_DistanceBottom метод. Получает или задает расстояние между нижней границей таблицы и окружающим текстом, в пунктах в C++."
type: docs
weight: 19000
url: /ru/cpp/aspose.words.tables/table/get_distancebottom/
---
## Table::get_DistanceBottom method


Получает или задаёт расстояние между нижней границей таблицы и окружающим текстом, в пунктах.

```cpp
double Aspose::Words::Tables::Table::get_DistanceBottom()
```


## Примеры



Показывает, как установить расстояние между границами таблицы и текстом.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Table wrapped by text.docx");

System::SharedPtr<Aspose::Words::Tables::Table> table = doc->get_FirstSection()->get_Body()->get_Tables()->idx_get(0);
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceTop());
ASPOSE_ASSERT_EQ(25.9, table->get_DistanceBottom());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceLeft());
ASPOSE_ASSERT_EQ(17.3, table->get_DistanceRight());

// Установить расстояние между таблицей и окружающим текстом.
table->set_DistanceLeft(24);
table->set_DistanceRight(24);
table->set_DistanceTop(3);
table->set_DistanceBottom(3);

doc->Save(get_ArtifactsDir() + u"Table.DistanceBetweenTableAndText.docx");
```

## См. также

* Class [Table](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
