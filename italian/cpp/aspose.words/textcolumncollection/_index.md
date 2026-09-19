---
title: "Classe Aspose::Words::TextColumnCollection"
linktitle: "TextColumnCollection"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::TextColumnCollection. Una raccolta di oggetti TextColumn che rappresentano tutte le colonne di testo in una sezione di un documento. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 71000
url: /it/cpp/aspose.words/textcolumncollection/
---
## TextColumnCollection class


Una raccolta di [TextColumn](../textcolumn/) oggetti che rappresentano tutte le colonne di testo in una sezione di un documento. Per saperne di più, visita l'articolo di documentazione [Working with Sections](https://docs.aspose.com/words/cpp/working-with-sections/).

```cpp
class TextColumnCollection : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Count](./get_count/)() | Restituisce il numero di colonne nella sezione di un documento. |
| [get_EvenlySpaced](./get_evenlyspaced/)() | Vero se le colonne di testo hanno larghezza uguale e sono equidistanti. |
| [get_LineBetween](./get_linebetween/)() | Quando **true**, aggiunge una linea verticale tra le colonne. |
| [get_Spacing](./get_spacing/)() | Quando le colonne sono equidistanti, ottiene o imposta la quantità di spazio tra ogni colonna in punti. |
| [get_Width](./get_width/)() | Quando le colonne sono equidistanti, ottiene la larghezza delle colonne. |
| [GetType](./gettype/)() const override |  |
| [idx_get](./idx_get/)(int32_t) | Restituisce una colonna di testo all'indice specificato. |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_EvenlySpaced](./set_evenlyspaced/)(bool) | Setter per [Aspose::Words::TextColumnCollection::get_EvenlySpaced](./get_evenlyspaced/). |
| [set_LineBetween](./set_linebetween/)(bool) | Setter per [Aspose::Words::TextColumnCollection::get_LineBetween](./get_linebetween/). |
| [set_Spacing](./set_spacing/)(double) | Setter per [Aspose::Words::TextColumnCollection::get_Spacing](./get_spacing/). |
| [SetCount](./setcount/)(int32_t) | Dispone il testo nel numero specificato di colonne di testo. |
| static [Type](./type/)() |  |
## Note


Usa [SetCount()](./setcount/) per impostare il numero di colonne di testo.

Per rendere tutte le colonne di larghezza uguale e equidistanti, imposta [EvenlySpaced](./get_evenlyspaced/) su **true** e specifica la quantità di spazio tra le colonne in [Spacing](./get_spacing/). MS Word calcolerà automaticamente le larghezze delle colonne.

Se hai impostato [EvenlySpaced](./get_evenlyspaced/) su **false**, devi specificare larghezza e spaziatura per ogni colonna singolarmente. Usa l'indicizzatore per accedere ai singoli oggetti [TextColumn](../textcolumn/).

Quando utilizzi larghezze di colonna personalizzate, assicurati che la somma di tutte le larghezze delle colonne e delle spaziature tra di esse sia uguale alla larghezza della pagina meno i margini sinistro e destro.

## Esempi



Mostra come creare più colonne equidistanti in una sezione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_Spacing(100);
columns->SetCount(2);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");

doc->Save(get_ArtifactsDir() + u"PageSetup.ColumnsSameWidth.docx");
```

## Vedi anche

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
