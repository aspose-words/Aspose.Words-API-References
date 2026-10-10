---
title: "Aspose::Words::TextColumn::get_Width metodo"
linktitle: "get_Width"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextColumn::get_Width metodo. Ottiene o imposta la larghezza della colonna di testo in punti in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/textcolumn/get_width/
---
## TextColumn::get_Width method


Ottiene o imposta la larghezza della colonna di testo in punti.

```cpp
double Aspose::Words::TextColumn::get_Width()
```


## Esempi



Mostra come creare colonne con spaziatura irregolare.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
System::SharedPtr<Aspose::Words::PageSetup> pageSetup = builder->get_PageSetup();

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = pageSetup->get_TextColumns();
columns->set_EvenlySpaced(false);
columns->SetCount(2);

// Determina la quantità di spazio disponibile per disporre le colonne.
double contentWidth = pageSetup->get_PageWidth() - pageSetup->get_LeftMargin() - pageSetup->get_RightMargin();

ASSERT_NEAR(470.30, contentWidth, 0.01);

// Imposta la prima colonna in modo che sia stretta.
System::SharedPtr<Aspose::Words::TextColumn> column = columns->idx_get(0);
column->set_Width(100);
column->set_SpaceAfter(20);

// Imposta la seconda colonna per occupare il resto dello spazio disponibile entro i margini della pagina.
column = columns->idx_get(1);
column->set_Width(contentWidth - column->get_Width() - column->get_SpaceAfter());

builder->Writeln(u"Narrow column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Wide column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.CustomColumnWidth.docx");
```

## Vedi anche

* Class [TextColumn](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
