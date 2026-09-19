---
title: "Classe Aspose::Words::Saving::TxtListIndentation"
linktitle: "TxtListIndentation"
second_title: "Riferimento API Aspose.Words per C++"
description: "Classe Aspose::Words::Saving::TxtListIndentation. Specifica come i livelli dell'elenco sono indentati quando il documento viene esportato in formato Text. Per saperne di più, visita l'articolo di documentazione in C++."
type: docs
weight: 32000
url: /it/cpp/aspose.words.saving/txtlistindentation/
---
## TxtListIndentation class


Specifica come i livelli dell'elenco sono indentati quando il documento viene esportato nel formato [Text](../../aspose.words/saveformat/). Per saperne di più, visita l'articolo di documentazione [Save a Document](https://docs.aspose.com/words/cpp/save-a-document/).

```cpp
class TxtListIndentation : public System::Object
```

## Metodi

| Metodo | Descrizione |
| --- | --- |
| [get_Character](./get_character/)() const | Ottiene o imposta quale carattere utilizzare per l'indentazione dei livelli dell'elenco. Il valore predefinito è '\\0', il che significa che non c'è indentazione. |
| [get_Count](./get_count/)() const | Ottiene o imposta quanti [Character](./get_character/) utilizzare come indentazione per un livello dell'elenco. Il valore predefinito è 0, il che significa nessuna indentazione. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_Character](./set_character/)(char16_t) | Metodo set per [Aspose::Words::Saving::TxtListIndentation::get_Character](./get_character/). |
| [set_Count](./set_count/)(int32_t) | Metodo set per [Aspose::Words::Saving::TxtListIndentation::get_Count](./get_count/). |
| [TxtListIndentation](./txtlistindentation/)() |  |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
