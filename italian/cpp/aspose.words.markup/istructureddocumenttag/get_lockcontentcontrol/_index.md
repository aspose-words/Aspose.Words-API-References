---
title: "Metodo Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl"
linktitle: "get_LockContentControl"
second_title: "Riferimento API Aspose.Words per C++"
description: "Metodo Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl. Quando impostato su true, questa proprietà impedirà a un utente di eliminare questo SDT in C++."
type: docs
weight: 6000
url: /it/cpp/aspose.words.markup/istructureddocumenttag/get_lockcontentcontrol/
---
## IStructuredDocumentTag::get_LockContentControl method


Quando impostata su true, questa proprietà impedirà a un utente di eliminare questo **SDT**.

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl()=0
```


## Esempi



Mostra come applicare restrizioni di modifica ai tag di documento strutturato.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Inserisci un tag di documento strutturato in testo semplice, che funge da casella di testo che invita l'utente a compilarlo.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Imposta la proprietà "LockContents" su "true" per impedire all'utente di modificare il contenuto di questa casella di testo.
tag->set_LockContents(true);
builder->Write(u"The contents of this structured document tag cannot be edited: ");
builder->InsertNode(tag);

tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Imposta la proprietà "LockContentControl" su "true" per impedire all'utente di
// cancellare manualmente questo tag di documento strutturato in Microsoft Word.
tag->set_LockContentControl(true);

builder->InsertParagraph();
builder->Write(u"This structured document tag cannot be deleted but its contents can be edited: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Lock.docx");
```

## Vedi anche

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
