---
title: "Aspose::Words::TextColumnCollection::get_LineBetween metodo"
linktitle: "get_LineBetween"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::TextColumnCollection::get_LineBetween metodo. Quando è true, aggiunge una linea verticale tra le colonne in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words/textcolumncollection/get_linebetween/
---
## TextColumnCollection::get_LineBetween method


Quando **true**, aggiunge una linea verticale tra le colonne.

```cpp
bool Aspose::Words::TextColumnCollection::get_LineBetween()
```


## Esempi



Mostra come separare le colonne con una linea verticale.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Configura l'oggetto PageSetup della sezione corrente per dividere il testo in più colonne.
// Imposta la proprietà "LineBetween" su "true" per inserire una linea divisoria tra le colonne.
// Imposta la proprietà "LineBetween" su "false" per lasciare vuoto lo spazio tra le colonne.
System::SharedPtr<Aspose::Words::TextColumnCollection> columns = builder->get_PageSetup()->get_TextColumns();
columns->set_LineBetween(lineBetween);
columns->SetCount(3);

builder->Writeln(u"Column 1.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 2.");
builder->InsertBreak(Aspose::Words::BreakType::ColumnBreak);
builder->Writeln(u"Column 3.");

doc->Save(get_ArtifactsDir() + u"PageSetup.VerticalLineBetweenColumns.docx");
```

## Vedi anche

* Class [TextColumnCollection](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
