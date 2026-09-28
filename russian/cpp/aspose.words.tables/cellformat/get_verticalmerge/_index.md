---
title: "Aspose::Words::Tables::CellFormat::get_VerticalMerge метод"
linktitle: "get_VerticalMerge"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::CellFormat::get_VerticalMerge метод. Указывает, как ячейка объединяется с другими ячейками вертикально в C++."
type: docs
weight: 14000
url: /ru/cpp/aspose.words.tables/cellformat/get_verticalmerge/
---
## CellFormat::get_VerticalMerge method


Указывает, как ячейка объединяется с другими ячейками по вертикали.

```cpp
Aspose::Words::Tables::CellMerge Aspose::Words::Tables::CellFormat::get_VerticalMerge()
```

## Примечания


Ячейки могут быть объединены вертикально только если их левый и правый границы идентичны.

Когда ячейки объединяются вертикально, области отображения объединённых ячеек консолидируются. Консолидированная область используется для отображения содержимого первой вертикально объединённой ячейки, а все остальные вертикально объединённые ячейки должны быть пустыми.

## Примеры



Показывает, как объединять ячейки таблицы вертикально.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Вставьте ячейку в первый столбец первой строки.
// Эта ячейка будет первой в диапазоне вертикально объединённых ячеек.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::First);
builder->Write(u"Text in merged cells.");

// Вставьте ячейку во второй столбец первой строки, затем завершите строку.
// Также настройте построитель, чтобы отключить вертикальное объединение в созданных ячейках.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();

// Вставьте ячейку в первый столбец второй строки.
// Вместо добавления текстового содержимого мы объединим эту ячейку с первой ячейкой, которую добавили непосредственно выше.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::Previous);

// Вставьте ещё одну независимую ячейку во второй столбец второй строки.
builder->InsertCell();
builder->get_CellFormat()->set_VerticalMerge(Aspose::Words::Tables::CellMerge::None);
builder->Write(u"Text in unmerged cell.");
builder->EndRow();
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"CellFormat.VerticalMerge.docx");
```

## См. также

* Enum [CellMerge](../../cellmerge/)
* Class [CellFormat](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
