---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_LockContents metod"
linktitle: "get_LockContents"
second_title: "Aspose.Words för C++ API‑referens"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_LockContents metod. När den är satt till true kommer denna egenskap att förhindra en användare från att redigera innehållet i detta SDT i C++."
type: docs
weight: 23000
url: /sv/cpp/aspose.words.markup/structureddocumenttag/get_lockcontents/
---
## StructuredDocumentTag::get_LockContents method


När den är satt till **true** kommer denna egenskap att förhindra en användare från att redigera innehållet i detta **SDT**.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_LockContents() override
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

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
