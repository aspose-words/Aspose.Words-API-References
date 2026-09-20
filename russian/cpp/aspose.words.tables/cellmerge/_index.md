---
title: "Aspose::Words::Tables::CellMerge enum"
linktitle: "CellMerge"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::CellMerge enum. Указывает, как ячейка в таблице объединяется с другими ячейками в C++."
type: docs
weight: 11000
url: /ru/cpp/aspose.words.tables/cellmerge/
---
## CellMerge enum


Указывает, как ячейка в таблице объединяется с другими ячейками.

```cpp
enum class CellMerge
```

### Значения

| Имя | Значение | Описание |
| --- | --- | --- |
| None | 0 | Ячейка не объединена. |
| First | 1 | Ячейка является первой ячейкой в диапазоне объединённых ячеек. |
| Назад | 2 | Ячейка объединяется с предыдущей ячейкой по горизонтали или вертикали. |


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

* Namespace [Aspose::Words::Tables](../)
* Library [Aspose.Words for C++](../../)
