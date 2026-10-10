---
title: "Aspose::Words::Markup::StructuredDocumentTag::get_LockContents Methode"
linktitle: "get_LockContents"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Markup::StructuredDocumentTag::get_LockContents method. Wenn sie auf true gesetzt ist, verhindert diese Eigenschaft, dass ein Benutzer den Inhalt dieses SDT in C++ bearbeitet."
type: docs
weight: 23000
url: /de/cpp/aspose.words.markup/structureddocumenttag/get_lockcontents/
---
## StructuredDocumentTag::get_LockContents method


Wenn auf **true** gesetzt, verhindert diese Eigenschaft, dass ein Benutzer den Inhalt dieses **SDT** bearbeitet.

```cpp
bool Aspose::Words::Markup::StructuredDocumentTag::get_LockContents() override
```


## Beispiele



Zeigt, wie Bearbeitungsbeschränkungen auf strukturierte Dokumentensteuerelemente angewendet werden.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie ein strukturiertes Dokumentensteuerelement für Nur-Text ein, das als Textfeld fungiert und den Benutzer auffordert, es auszufüllen.
auto tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Setzen Sie die "LockContents"-Eigenschaft auf "true", um zu verhindern, dass der Benutzer den Inhalt dieses Textfelds bearbeitet.
tag->set_LockContents(true);
builder->Write(u"The contents of this structured document tag cannot be edited: ");
builder->InsertNode(tag);

tag = System::MakeObject<Aspose::Words::Markup::StructuredDocumentTag>(doc, Aspose::Words::Markup::SdtType::PlainText, Aspose::Words::Markup::MarkupLevel::Inline);

// Setzen Sie die "LockContentControl"-Eigenschaft auf "true", um zu verhindern, dass der Benutzer
// dieses strukturierte Dokumentensteuerelement manuell in Microsoft Word löscht.
tag->set_LockContentControl(true);

builder->InsertParagraph();
builder->Write(u"This structured document tag cannot be deleted but its contents can be edited: ");
builder->InsertNode(tag);

doc->Save(get_ArtifactsDir() + u"StructuredDocumentTag.Lock.docx");
```

## Siehe auch

* Class [StructuredDocumentTag](../)
* Namespace [Aspose::Words::Markup](../../)
* Library [Aspose.Words for C++](../../../)
