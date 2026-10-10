---
title: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag-Methode"
linktitle: "MoveToStructuredDocumentTag"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag-Methode. Bewegt den Cursor zum strukturierten Dokument-Tag in C++."
type: docs
weight: 61000
url: /de/cpp/aspose.words/documentbuilder/movetostructureddocumenttag/
---
## DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr\<Aspose::Words::Markup::StructuredDocumentTag\>\&, int32_t) method


Bewegt den Cursor zum strukturierten Dokument-Tag.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(const System::SharedPtr<Aspose::Words::Markup::StructuredDocumentTag> &structuredDocumentTag, int32_t characterIndex)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| structuredDocumentTag | const System::SharedPtr\\<Aspose::Words::Markup::StructuredDocumentTag\\>\\& | Der strukturierte Dokument-Tag, zu dem bewegt werden soll. |
| characterIndex | int32_t | Der Index des Zeichens innerhalb des strukturierten Dokument‑Tags. Ein negativer Wert ermöglicht die Angabe einer Position vom Ende des strukturierten Dokument‑Tags aus. Verwenden Sie -1, um zum Ende des strukturierten Dokument‑Tags zu springen. Befindet sich der strukturierte Dokument‑Tag auf Blockebene und möchten Sie den Cursor zum Ende seines letzten Absatzes bewegen, geben Sie -2 an. |

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

* Class [StructuredDocumentTag](../../../aspose.words.markup/structureddocumenttag/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::MoveToStructuredDocumentTag(int32_t, int32_t) method


Bewegt den Cursor zu einem strukturierten Dokument-Tag im aktuellen Abschnitt.

```cpp
void Aspose::Words::DocumentBuilder::MoveToStructuredDocumentTag(int32_t structuredDocumentTagIndex, int32_t characterIndex)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| structuredDocumentTagIndex | int32_t | Der Index des strukturierten Dokument‑Tags, zu dem bewegt werden soll. |
| characterIndex | int32_t | Der Index des Zeichens innerhalb des strukturierten Dokument‑Tags. Ein negativer Wert ermöglicht die Angabe einer Position vom Ende des strukturierten Dokument‑Tags aus. Verwenden Sie -1, um zum Ende des strukturierten Dokument‑Tags zu springen. Befindet sich der strukturierte Dokument‑Tag auf Blockebene und möchten Sie den Cursor zum Ende seines letzten Absatzes bewegen, geben Sie -2 an. |
## Hinweise


Die Navigation wird innerhalb der aktuellen Story des aktuellen Abschnitts durchgeführt. Das bedeutet, wenn Sie den Cursor zur primären Überschrift des ersten Abschnitts bewegt haben, dann gibt *structuredDocumentTagIndex* den Index des strukturierten Dokumenten-Tags innerhalb dieser Überschrift dieses Abschnitts an.

Wenn *structuredDocumentTagIndex* größer oder gleich 0 ist, gibt es einen Index vom Anfang des Abschnitts an, wobei 0 das erste strukturierte Dokumenten-Tag ist. Wenn *structuredDocumentTagIndex* kleiner als 0 ist, gibt es einen Index vom Ende des Abschnitts an, wobei -1 das letzte strukturierte Dokumenten-Tag ist.

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
