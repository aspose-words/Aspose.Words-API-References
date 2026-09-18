---
title: "Aspose::Words::InlineStory::get_Paragraphs-Methode"
linktitle: "get_Paragraphs"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::InlineStory::get_Paragraphs-Methode. Gibt eine Sammlung von Absätzen zurück, die unmittelbare Kinder der Story in C++ sind."
type: docs
weight: 10000
url: /de/cpp/aspose.words/inlinestory/get_paragraphs/
---
## InlineStory::get_Paragraphs method


Ermittelt eine Sammlung von Absätzen, die direkte Kindknoten der Geschichte sind.

```cpp
System::SharedPtr<Aspose::Words::ParagraphCollection> Aspose::Words::InlineStory::get_Paragraphs() override
```


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


Zeigt, wie man einem Absatz einen Kommentar hinzufügt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);
builder->Write(u"Hello world!");

auto comment = System::MakeObject<Aspose::Words::Comment>(doc, u"John Doe", u"JD", System::DateTime::get_Today());
builder->get_CurrentParagraph()->AppendChild<System::SharedPtr<Aspose::Words::Comment>>(comment);
builder->MoveTo(comment->AppendChild<System::SharedPtr<Aspose::Words::Paragraph>>(System::MakeObject<Aspose::Words::Paragraph>(doc)));
builder->Write(u"Comment text.");

ASSERT_EQ(System::DateTime::get_Today(), comment->get_DateTime());

// In Microsoft Word können wir diesen Kommentar im Dokumentenkörper rechtsklicken, um ihn zu bearbeiten oder darauf zu antworten.
doc->Save(get_ArtifactsDir() + u"InlineStory.AddComment.docx");
```

## Siehe auch

* Class [ParagraphCollection](../../paragraphcollection/)
* Class [InlineStory](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
