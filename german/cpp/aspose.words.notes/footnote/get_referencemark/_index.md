---
title: "Aspose::Words::Notes::Footnote::get_ReferenceMark method"
linktitle: "get_ReferenceMark"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::Footnote::get_ReferenceMark-Methode. Gibt/Setzt das benutzerdefinierte Referenzzeichen, das für diese Fußnote verwendet wird. Der Standardwert ist ein leerer String, was bedeutet, dass automatisch nummerierte Fußnoten in C++ verwendet werden."
type: docs
weight: 7000
url: /de/cpp/aspose.words.notes/footnote/get_referencemark/
---
## Footnote::get_ReferenceMark method


Liest/setzt das benutzerdefinierte Referenzzeichen, das für diese Fußnote verwendet wird. Der Standardwert ist **empty string**, was bedeutet, dass automatisch nummerierte Fußnoten verwendet werden.

```cpp
System::String Aspose::Words::Notes::Footnote::get_ReferenceMark() const
```

## Hinweise


Wenn diese Eigenschaft auf **empty string** oder **null** gesetzt ist, wird die [IsAuto](../get_isauto/)-Eigenschaft automatisch auf **true** gesetzt; wird sie auf etwas anderes gesetzt, wird die [IsAuto](../get_isauto/)-Eigenschaft auf **false** gesetzt.

Das RTF-Format kann nur 1 Symbol als benutzerdefiniertes Referenzzeichen speichern, sodass beim Export nur das erste Symbol geschrieben wird und die übrigen verworfen werden.

## Beispiele



Zeigt, wie man Fußnoten einfügt und anpasst.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie Text hinzu und referenzieren Sie ihn mit einer Fußnote. Diese Fußnote setzt ein kleines hochgestelltes Referenzzeichen
// nach dem Text, auf den sie sich bezieht, und erstellt einen Eintrag unterhalb des Haupttextes am unteren Rand der Seite.
// Dieser Eintrag enthält das Referenzzeichen der Fußnote und den Referenztext,
// den wir an die Methode "InsertFootnote" des Dokumenten‑Builders übergeben.
builder->Write(u"Main body text.");
System::SharedPtr<Aspose::Words::Notes::Footnote> footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Wenn diese Eigenschaft auf "true" gesetzt ist, dann ist das Referenzzeichen unserer Fußnote
// ihre Indexposition unter allen Fußnoten des Abschnitts.
// Dies ist die erste Fußnote, sodass das Referenzzeichen "1" lautet.
ASSERT_TRUE(footnote->get_IsAuto());

// Wir können den Dokumenten‑Builder in die Fußnote verschieben, um ihren Referenztext zu bearbeiten.
builder->MoveTo(footnote->get_FirstParagraph());
builder->Write(u" More text added by a DocumentBuilder.");
builder->MoveToDocumentEnd();

ASSERT_EQ(u"\u0002 Footnote text. More text added by a DocumentBuilder.", footnote->GetText().Trim());

builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

// Wir können ein benutzerdefiniertes Referenzzeichen festlegen, das die Fußnote anstelle ihrer Indexnummer verwendet.
footnote->set_ReferenceMark(u"RefMark");

ASSERT_FALSE(footnote->get_IsAuto());

// Ein Lesezeichen mit dem "IsAuto"‑Flag, das auf true gesetzt ist, zeigt weiterhin seinen echten Index
// auch wenn vorherige Lesezeichen benutzerdefinierte Referenzzeichen anzeigen, sodass das Referenzzeichen dieses Lesezeichens "3" sein wird.
builder->Write(u" More main body text.");
footnote = builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote text.");

ASSERT_TRUE(footnote->get_IsAuto());

doc->Save(get_ArtifactsDir() + u"InlineStory.AddFootnote.docx");
```

## Siehe auch

* Class [Footnote](../)
* Namespace [Aspose::Words::Notes](../../)
* Library [Aspose.Words for C++](../../../)
