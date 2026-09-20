---
title: "Aspose::Words::Drawing::Charts::Chart::get_SourceFullName метод"
linktitle: "get_SourceFullName"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::Drawing::Charts::Chart::get_SourceFullName. Получает путь и имя файла xls/xlsx, к которому привязан эта диаграмма, в C++."
type: docs
weight: 7000
url: /ru/cpp/aspose.words.drawing.charts/chart/get_sourcefullname/
---
## Chart::get_SourceFullName method


Получает путь и имя файла xls/xlsx, к которому привязана эта диаграмма.

```cpp
System::String Aspose::Words::Drawing::Charts::Chart::get_SourceFullName()
```


## Примеры



Показывает, как получить/установить полное имя внешнего документа xls/xlsx, если диаграмма связана.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Shape with linked chart.docx");

auto shape = System::ExplicitCast<Aspose::Words::Drawing::Shape>(doc->GetChild(Aspose::Words::NodeType::Shape, 0, true));

System::String sourceFullName = shape->get_Chart()->get_SourceFullName();
ASSERT_TRUE(sourceFullName.Contains(u"Examples\\Data\\Spreadsheet.xlsx"));
```

## См. также

* Class [Chart](../)
* Namespace [Aspose::Words::Drawing::Charts](../../)
* Library [Aspose.Words for C++](../../../)
