---
title: "Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag-Methode"
linktitle: "get_IsAtEndOfStructuredDocumentTag"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag method. Gibt true zurück, wenn sich der Cursor am Ende eines strukturierten Dokument-Tags befindet, in C++."
type: docs
weight: 19000
url: /de/cpp/aspose.words/documentbuilder/get_isatendofstructureddocumenttag/
---
## DocumentBuilder::get_IsAtEndOfStructuredDocumentTag method


Gibt **true** zurück, wenn sich der Cursor am Ende eines strukturierten Dokument‑Tags befindet.

```cpp
bool Aspose::Words::DocumentBuilder::get_IsAtEndOfStructuredDocumentTag()
```


## Beispiele



Zeigt, wie der Cursor von [DocumentBuilder](../) innerhalb eines strukturierten Dokument‑Tags bewegt wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Structured document tags.docx");
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Es gibt mehrere Möglichkeiten, den Cursor zu bewegen:
// 1 -  Zum ersten Zeichen des strukturierten Dokument‑Tags nach Index bewegen.
builder->MoveToStructuredDocumentTag(1, 1);

// 2 -  Zum ersten Zeichen des strukturierten Dokument‑Tags nach Objekt bewegen.
auto tag = System::ExplicitCast<Aspose::Words::Markup::StructuredDocumentTag>(doc->GetChild(Aspose::Words::NodeType::StructuredDocumentTag, 2, true));
builder->MoveToStructuredDocumentTag(tag, 1);
builder->Write(u" New text.");

ASSERT_EQ(u"R New text.ichText", tag->GetText().Trim());

// 3 -  Zum Ende des zweiten strukturierten Dokument‑Tags bewegen.
builder->MoveToStructuredDocumentTag(1, -1);
ASSERT_TRUE(builder->get_IsAtEndOfStructuredDocumentTag());

// Den aktuell ausgewählten strukturierten Dokument‑Tag abrufen.
builder->get_CurrentStructuredDocumentTag()->set_Color(System::Drawing::Color::get_Green());

doc->Save(get_ArtifactsDir() + u"Document.MoveToStructuredDocumentTag.docx");
```

## Siehe auch

* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
