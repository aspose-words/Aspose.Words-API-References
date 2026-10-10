---
title: "Metodo get_ContextTableFormatting di Aspose::Words::DocumentBuilderOptions"
linktitle: "get_ContextTableFormatting"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo get_ContextTableFormatting di Aspose::Words::DocumentBuilderOptions. Vero se la formattazione applicata al contenuto della tabella non influisce sulla formattazione del contenuto che lo segue. Il valore predefinito è true in C++."
type: docs
weight: 3000
url: /it/cpp/aspose.words/documentbuilderoptions/get_contexttableformatting/
---
## DocumentBuilderOptions::get_ContextTableFormatting method


Vero se la formattazione applicata al contenuto della tabella non influisce sulla formattazione del contenuto che lo segue. Il valore predefinito è **true**.

```cpp
bool Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting() const
```


## Esempi



Mostra come ignorare la formattazione della tabella per il contenuto successivo.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builderOptions = System::MakeObject<Aspose::Words::DocumentBuilderOptions>();
builderOptions->set_ContextTableFormatting(true);
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc, builderOptions);

// Aggiunge contenuto prima della tabella.
// La dimensione predefinita del carattere è 12.
builder->Writeln(u"Font size 12 here.");
builder->StartTable();
builder->InsertCell();
// Modifica la dimensione del carattere all'interno della tabella.
builder->get_Font()->set_Size(5);
builder->Write(u"Font size 5 here");
builder->InsertCell();
builder->Write(u"Font size 5 here");
builder->EndRow();
builder->EndTable();

// Se ContextTableFormatting è vero, la formattazione della tabella non viene applicata al contenuto successivo.
// Se ContextTableFormatting è falso, la formattazione della tabella viene applicata al contenuto successivo.
builder->Writeln(u"Font size 12 here.");

doc->Save(get_ArtifactsDir() + u"Table.ContextTableFormatting.docx");
```

## Vedi anche

* Class [DocumentBuilderOptions](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
