---
title: "Classe Aspose::Words::DocumentBuilderOptions"
linktitle: "DocumentBuilderOptions"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::DocumentBuilderOptions. Consente di specificare opzioni aggiuntive per il processo di creazione del documento in C++."
type: docs
weight: 22500
url: /it/cpp/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class


Consente di specificare opzioni aggiuntive per il processo di creazione del documento.

```cpp
class DocumentBuilderOptions : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [DocumentBuilderOptions](./documentbuilderoptions/)() |  |
| [get_ContextTableFormatting](./get_contexttableformatting/)() const | Vero se la formattazione applicata al contenuto della tabella non influisce sulla formattazione del contenuto che lo segue. Il valore predefinito è **true**. |
| [get_DesignMode](./get_designmode/)() const | Corrisponde alla Modalità Progettazione in Microsoft Word. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_ContextTableFormatting](./set_contexttableformatting/)(bool) | Setter per [Aspose::Words::DocumentBuilderOptions::get_ContextTableFormatting](./get_contexttableformatting/). |
| [set_DesignMode](./set_designmode/)(bool) | Corrisponde alla Modalità Progettazione in Microsoft Word. |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
