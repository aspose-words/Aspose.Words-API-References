---
title: "Aspose::Words::TextColumnCollection::SetCount metodo"
linktitle: "SetCount"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextColumnCollection::SetCount metodo. Dispone il testo nel numero specificato di colonne di testo in C++."
type: docs
weight: 13000
url: /it/cpp/aspose.words/textcolumncollection/setcount/
---
## TextColumnCollection::SetCount method


Dispone il testo nel numero specificato di colonne di testo.

```cpp
void Aspose::Words::TextColumnCollection::SetCount(int32_t newCount)
```


| Parametro | Tipo | Descrizione |
| --- | --- | --- |
| newCount | int32_t | Il numero di colonne in cui il testo deve essere disposto. |
## Note


Quando [EvenlySpaced](../get_evenlyspaced/) è **false** e aumenti il numero di colonne, vengono creati nuovi oggetti [TextColumn](../../textcolumn/) con larghezza e spaziatura zero. È necessario impostare larghezza e spaziatura per le nuove colonne.

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

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
