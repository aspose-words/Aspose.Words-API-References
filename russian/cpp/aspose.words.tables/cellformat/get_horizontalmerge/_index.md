---
title: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge метод"
linktitle: "get_HorizontalMerge"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::CellFormat::get_HorizontalMerge метод. Указывает, как ячейка объединяется горизонтально с другими ячейками в строке в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.tables/cellformat/get_horizontalmerge/
---
## CellFormat::get_HorizontalMerge method


Указывает, как ячейка объединяется горизонтально с другими ячейками в строке.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_HorizontalMerge()
```


## Примеры



Показывает, как объединять ячейки таблицы горизонтально.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте ячейку в первый столбец первой строки.
// Эта ячейка будет первой в диапазоне горизонтально объединённых ячеек.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Вставьте ячейку во второй столбец первой строки. Вместо добавления текстового содержимого,
// мы объединим эту ячейку с первой ячейкой, которую добавили непосредственно слева.
builder->InsertCell();
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::Previous);
builder->EndRow();

// Вставьте ещё две не объединённые ячейки во вторую строку.
builder->get_CellFormat()->set_HorizontalMerge(Aspose::Words::Tables::CellMerge::None);
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->InsertCell();
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.HorizontalMerge.docx");
```

## См. также

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
