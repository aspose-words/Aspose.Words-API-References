---
title: "Метод Aspose::Words::DocumentBuilder::MoveToCell"
linktitle: "MoveToCell"
second_title: "Справочник API Aspose.Words для C++"
description: "Метод Aspose::Words::DocumentBuilder::MoveToCell. Перемещает курсор в ячейку таблицы в текущем разделе в C++."
type: docs
weight: 53000
url: /ru/cpp/aspose.words/documentbuilder/movetocell/
---
## DocumentBuilder::MoveToCell method


Перемещает курсор к ячейке таблицы в текущем разделе.

```cpp
void Aspose::Words::DocumentBuilder::MoveToCell(int32_t tableIndex, int32_t rowIndex, int32_t columnIndex, int32_t characterIndex)
```


| Параметр | Тип | Описание |
| --- | --- | --- |
| tableIndex | int32_t | Индекс таблицы, к которой нужно перейти. |
| rowIndex | int32_t | Индекс строки в таблице. |
| columnIndex | int32_t | Индекс столбца в таблице. |
| characterIndex | int32_t | Индекс символа внутри ячейки. Отрицательное значение позволяет указать позицию с конца ячейки. Используйте -1, чтобы переместиться в конец ячейки. |
## Примечания


Навигация выполняется внутри текущей истории текущего раздела.

Для параметров индекса, когда индекс больше или равен 0, он указывает позицию с начала, где 0 — первый элемент. Когда индекс меньше 0, он указывает позицию с конца, где -1 — последний элемент.

## Примеры



Показывает, как переместить курсор DocumentBuilder в ячейку таблицы.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте пустую таблицу 2×2.
builder->StartTable();
builder->InsertCell();
builder->InsertCell();
builder->EndRow();
builder->InsertCell();
builder->InsertCell();
builder->EndTable();

// Поскольку мы завершили таблицу методом EndTable,
// курсор DocumentBuilder в данный момент находится за пределами таблицы.
// Этот курсор выполняет ту же функцию, что и мигающий текстовый курсор Microsoft Word.
// Он также может быть перемещён в другое место документа с помощью методов MoveTo объекта builder.
// Мы можем переместить курсор обратно внутрь таблицы в конкретную ячейку.
builder->MoveToCell(0, 1, 1, 0);
builder->Write(u"Column 2, cell 2.");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.MoveToCell.docx");
```

## См. также

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
