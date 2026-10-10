---
title: "Aspose::Words::DocumentBuilder::get_Italic method"
linktitle: "get_Italic"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::DocumentBuilder::get_Italic method. True se il carattere è formattato in corsivo in C++."
type: docs
weight: 21000
url: /it/cpp/aspose.words/documentbuilder/get_italic/
---
## DocumentBuilder::get_Italic method


Vero se il carattere è formattato in corsivo.

```cpp
bool Aspose::Words::DocumentBuilder::get_Italic()
```


## Esempi



Mostra come riempire i MERGEFIELD con i dati usando un document builder invece di un'unione di stampa.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci alcuni MERGEFIELD, che accettano dati dalle colonne con lo stesso nome in una fonte dati durante un'unione di stampa,
// e poi riempili manualmente.
builder->InsertField(u" MERGEFIELD Chairman ");
builder->InsertField(u" MERGEFIELD ChiefFinancialOfficer ");
builder->InsertField(u" MERGEFIELD ChiefTechnologyOfficer ");

builder->MoveToMergeField(u"Chairman");
builder->set_Bold(true);
builder->Writeln(u"John Doe");

builder->MoveToMergeField(u"ChiefFinancialOfficer");
builder->set_Italic(true);
builder->Writeln(u"Jane Doe");

builder->MoveToMergeField(u"ChiefTechnologyOfficer");
builder->set_Italic(true);
builder->Writeln(u"John Bloggs");

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.FillMergeFields.docx");
```

## Vedi anche

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
