---
title: "Aspose::Words::Tables::CellFormat::SetPaddings метод"
linktitle: "SetPaddings"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::CellFormat::SetPaddings метод. Устанавливает количество пространства (в пунктах), которое добавляется слева/сверху/справа/снизу от содержимого ячейки в C++."
type: docs
weight: 31000
url: /ru/cpp/aspose.words.tables/cellformat/setpaddings/
---
## CellFormat::SetPaddings method


Устанавливает количество пространства (в пунктах), добавляемого слева/сверху/справа/снизу к содержимому ячейки.

```cpp
void Aspose::Words::Tables::CellFormat::SetPaddings(double leftPadding, double topPadding, double rightPadding, double bottomPadding)
```


## Примеры



Показывает, как добавить отступы к содержимому ячейки с помощью пробелов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Установите расстояние отступа (в пунктах) между границей и текстовым содержимым
// для каждой ячейки таблицы, которую мы создаём с помощью Document Builder.
builder->get_CellFormat()->SetPaddings(5, 10, 40, 50);

// Создайте таблицу с одной ячейкой, содержимое которой будет иметь отступы пробелами.
builder->StartTable();
builder->InsertCell();
builder->Write(System::String(u"Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. ") + u"Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat.");

doc->Save(get_ArtifactsDir() + u"CellFormat.Padding.docx");
```

## См. также

* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
