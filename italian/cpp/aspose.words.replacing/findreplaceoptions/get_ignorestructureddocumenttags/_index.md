---
title: "Metodo Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags"
linktitle: "get_IgnoreStructuredDocumentTags"
second_title: "Riferimento API Aspose.Words per C++"
description: "Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags method. Ottiene o imposta un valore booleano che indica se ignorare il contenuto di StructuredDocumentTag. Il valore predefinito è false in C++."
type: docs
weight: 12000
url: /it/cpp/aspose.words.replacing/findreplaceoptions/get_ignorestructureddocumenttags/
---
## FindReplaceOptions::get_IgnoreStructuredDocumentTags method


Ottiene o imposta un valore booleano che indica se ignorare il contenuto di [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/). Il valore predefinito è **false**.

```cpp
bool Aspose::Words::Replacing::FindReplaceOptions::get_IgnoreStructuredDocumentTags() const
```

## Note


Quando questa opzione è impostata su **true**, il contenuto di [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) verrà trattato come testo semplice.

Altrimenti, [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/) verrà elaborato come [Story](../../../aspose.words/story/) autonomo e il modello di sostituzione verrà cercato separatamente per ciascun [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), in modo che se il modello attraversa un [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/), la sostituzione non verrà eseguita per tale modello.

## Esempi



Mostra come ignorare il contenuto dei tag durante la sostituzione.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");

// Questo paragrafo contiene SDT.
auto p = System::ExplicitCast<Aspose::Words::Paragraph>(doc->get_FirstSection()->get_Body()->GetChild(Aspose::Words::NodeType::Paragraph, 2, true));
System::String textToSearch = p->ToString(Aspose::Words::SaveFormat::Text).Trim();

auto options = System::MakeObject<Aspose::Words::Replacing::FindReplaceOptions>();
options->set_IgnoreStructuredDocumentTags(true);
doc->get_Range()->Replace(textToSearch, u"replacement", options);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IgnoreStructuredDocumentTags.docx");
```

## Vedi anche

* Class [FindReplaceOptions](../)
* Namespace [Aspose::Words::Replacing](../../)
* Library [Aspose.Words for C++](../../../)
