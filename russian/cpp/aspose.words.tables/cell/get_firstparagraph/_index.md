---
title: "Aspose::Words::Tables::Cell::get_FirstParagraph method"
linktitle: "get_FirstParagraph"
second_title: "Справочник API Aspose.Words для C++"
description: "Aspose::Words::Tables::Cell::get_FirstParagraph method. Получает первый абзац среди непосредственных дочерних элементов в C++."
type: docs
weight: 6000
url: /ru/cpp/aspose.words.tables/cell/get_firstparagraph/
---
## Cell::get_FirstParagraph method


Получает первый абзац среди непосредственных дочерних элементов.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Tables::Cell::get_FirstParagraph()
```


## Примеры



Показывает, как создать вложенную таблицу с помощью построителя документов.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Создайте внешнюю таблицу.
System::SharedPtr<Aspose::Words::Tables::Cell> cell = builder->InsertCell();
builder->Writeln(u"Outer Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Outer Table Cell 2");
builder->EndTable();

// Перейдите к первой ячейке внешней таблицы, затем создайте другую таблицу внутри ячейки.
builder->MoveTo(cell->get_FirstParagraph());
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 2");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertNestedTable.docx");
```

## См. также

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
