---
title: "Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl metod"
linktitle: "get_LockContentControl"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl metod. När den är satt till true kommer denna egenskap att förhindra att en användare kan ta bort denna SDT i C++."
type: docs
weight: 6000
url: /sv/cpp/aspose.words.markup/istructureddocumenttag/get_lockcontentcontrol/
---
## IStructuredDocumentTag::get_LockContentControl method


När den sätts till true kommer denna egenskap att förhindra en användare från att ta bort denna **SDT**.

```cpp
virtual bool Aspose::Words::Markup::IStructuredDocumentTag::get_LockContentControl()=0
```


## Exempel



Visar hur man tillämpar redigeringsrestriktioner på strukturerade dokumenttaggar.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Infoga en vanlig text strukturerad dokumenttagg, som fungerar som en textruta som uppmanar användaren att fylla i den.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Ställ in egenskapen "LockContents" till "true" för att förhindra användaren från att redigera innehållet i den här textrutan.
tag->set_LockContents(true);
builder->Write(u"The contents of this structured document tag cannot be edited: ");
builder->InsertNode(tag);

tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Ställ in egenskapen "LockContentControl" till "true" för att förhindra användaren från
// att manuellt ta bort denna strukturerade dokumenttagg i Microsoft Word.
tag->set_LockContentControl(true);

builder->InsertParagraph();
builder->Write(u"This structured document tag cannot be deleted but its contents can be edited: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Lock.docx");
```

## Se även

* Interface [IStructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
