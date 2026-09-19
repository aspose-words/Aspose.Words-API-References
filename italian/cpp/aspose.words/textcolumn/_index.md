---
title: "Aspose::Words::TextColumn class"
linktitle: "TextColumn"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextColumn class. Rappresenta una singola colonna di testo. TextColumn è un membro della collezione TextColumnCollection. La collezione TextColumn include tutte le colonne in una sezione di un documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 70000
url: /it/cpp/aspose.words/textcolumn/
---
## TextColumn class


Rappresenta una singola colonna di testo. [TextColumn](./) è un membro della collezione [TextColumnCollection](../textcolumncollection/). La collezione [TextColumn](./) include tutte le colonne in una sezione di un documento. Per saperne di più, visita l'articolo di documentazione [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumn : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_SpaceAfter](./get_spaceafter/)() | Ottiene o imposta lo spazio tra questa colonna e la colonna successiva in punti. Non richiesto per l'ultima colonna. |
| [get_Width](./get_width/)() | Ottiene o imposta la larghezza della colonna di testo in punti. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_SpaceAfter](./set_spaceafter/)(double) | Metodo setter per [Aspose::Words::TextColumn::get_SpaceAfter](./get_spaceafter/). |
| [set_Width](./set_width/)(double) | Metodo setter per [Aspose::Words::TextColumn::get_Width](./get_width/). |
| static [Type](./type/)() |  |
## Note


[TextColumn](./) objects are only used to specify columns with custom width and spacing. If you want the columns in the document to be of equal width, set TextColumns.[EvenlySpaced](../textcolumncollection/get_evenlyspaced/) to **true**.

Quando viene creata una nuova [TextColumn](./) la sua larghezza e spaziatura sono impostate a zero.

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
