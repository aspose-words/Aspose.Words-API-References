---
title: "Metodo Aspose::Words::Saving::TxtListIndentation::get_Count"
linktitle: "get_Count"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Saving::TxtListIndentation::get_Count. Ottiene o imposta quanti Character da usare come rientro per un livello di elenco. Il valore predefinito è 0, il che significa nessun rientro in C++."
type: docs
weight: 4000
url: /it/cpp/aspose.words.saving/txtlistindentation/get_count/
---
## TxtListIndentation::get_Count method


Ottiene o imposta quanti [Character](../get_character/) da usare come rientro per un livello di elenco. Il valore predefinito è 0, il che significa nessun rientro.

```cpp
int32_t Aspose::Words::Saving::TxtListIndentation::get_Count() const
```


## Esempi



Mostra come configurare l'indentazione dell'elenco quando si salva un documento in testo semplice.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Crea un elenco con tre livelli di indentazione.
builder->get_ListFormat()->ApplyNumberDefault();
builder->Writeln(u"Item 1");
builder->get_ListFormat()->ListIndent();
builder->Writeln(u"Item 2");
builder->get_ListFormat()->ListIndent();
builder->Write(u"Item 3");

// Crea un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo semplice.
auto txtSaveOptions = System::MakeObject<Aspose::Words::Saving::TxtSaveOptions>();

// Imposta la proprietà "Character" per assegnare un carattere da utilizzare
// per il riempimento che simula l'indentazione dell'elenco in testo semplice.
txtSaveOptions->get_ListIndentation()->set_Character(u' ');

// Imposta la proprietà "Count" per specificare il numero di volte
// per posizionare il carattere di riempimento per ogni livello di indentazione dell'elenco.
txtSaveOptions->get_ListIndentation()->set_Count(3);

doc->Save(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt", txtSaveOptions);

System::String docText = System::IO::File::ReadAllText(get_ArtifactsDir() + u"TxtSaveOptions.TxtListIndentation.txt");
System::String newLine = System::Environment::get_NewLine();

ASSERT_EQ(System::String::Format(u"1. Item 1{0}", newLine) + System::String::Format(u"   a. Item 2{0}", newLine) + System::String::Format(u"      i. Item 3{0}", newLine), docText);
```

## Vedi anche

* Class [TxtListIndentation](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
