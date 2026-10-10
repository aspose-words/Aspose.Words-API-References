---
title: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary"
linktitle: "get_IsTemporary"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary. Specifica se questo SDT deve essere rimosso dal documento WordProcessingML quando il suo contenuto viene modificato in C++."
type: docs
weight: 19000
url: /it/cpp/aspose.words.markup/structureddocumenttag/get_istemporary/
---
## StructuredDocumentTag::get_IsTemporary method


Specifica se questo **SDT** deve essere rimosso dal documento WordProcessingML quando il suo contenuto viene modificato.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_IsTemporary() const
```


## Esempi



Mostra come creare controlli monouso.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();

// Inserisci un tag di documento strutturato di testo semplice,
// che fungerà da modulo di testo semplice in cui l'utente può inserire testo.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Imposta la proprietà "IsTemporary" su "true" per far scomparire il tag di documento strutturato e
// assimilarne il contenuto nel documento dopo che l'utente lo ha modificato una volta in Microsoft Word.
// Imposta la proprietà "IsTemporary" su "false" per consentire all'utente di modificare il contenuto
// del tag di documento strutturato un numero illimitato di volte.
tag->set_IsTemporary(isTemporary);

auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Please enter text: ");
builder->InsertNode(tag);

// Inserisci un altro tag di documento strutturato sotto forma di casella di controllo e imposta il suo stato predefinito su "checked".
tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::Checkbox, Aspose::Words::Markup::MarkupLevel::Inline);
tag->set_Checked(true);

// Imposta la proprietà "IsTemporary" su "true" per far diventare la casella di controllo un simbolo
// una volta che l'utente fa clic su di essa in Microsoft Word.
// Imposta la proprietà "IsTemporary" su "false" per consentire all'utente di fare clic sulla casella di controllo un numero illimitato di volte.
tag->set_IsTemporary(isTemporary);

builder->Write(u"\nPlease click the check box: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.IsTemporary.docx");
```

## Vedi anche

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
