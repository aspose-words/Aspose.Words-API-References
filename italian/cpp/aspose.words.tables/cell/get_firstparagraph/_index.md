---
title: "Metodo Aspose::Words::Tables::Cell::get_FirstParagraph"
linktitle: "get_FirstParagraph"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Tables::Cell::get_FirstParagraph. Ottiene il primo paragrafo tra i figli immediati in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.tables/cell/get_firstparagraph/
---
## Cell::get_FirstParagraph method


Ottiene il primo paragrafo tra i figli immediati.

```cpp
System::SharedPtr<Aspose::Words::Paragraph> Aspose::Words::Tables::Cell::get_FirstParagraph()
```


## Esempi



Mostra come creare una tabella nidificata usando un document builder.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea la tabella esterna.
System::SharedPtr<Aspose::Words::Tables::Cell> cell = builder->InsertCell();
builder->Writeln(u"Outer Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Outer Table Cell 2");
builder->EndTable();

// Sposta alla prima cella della tabella esterna, quindi crea un'altra tabella all'interno della cella.
builder->MoveTo(cell->get_FirstParagraph());
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 1");
builder->InsertCell();
builder->Writeln(u"Inner Table Cell 2");
builder->EndTable();

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertNestedTable.docx");
```

## Vedi anche

* Class [Paragraph](../../../aspose.words/paragraph/)
* Class [Cell](../)
* Namespace [Aspose::Words::Tables](../../)
* Library [Aspose.Words for C++](../../../)
