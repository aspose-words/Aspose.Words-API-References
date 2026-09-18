---
title: "Aspose::Words::Notes::FootnoteType enum"
linktitle: "FootnoteType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Notes::FootnoteType enum. Gibt an, ob es sich in C++ um eine Fußnote oder eine Endnote handelt."
type: docs
weight: 7000
url: /de/cpp/aspose.words.notes/footnotetype/
---
## FootnoteType enum


Gibt an, ob es sich um eine Fußnote oder eine Endnote handelt.

```cpp
enum class FootnoteType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Footnote | 0 | Das Objekt ist eine Fußnote. |
| Endnote | 1 | Das Objekt ist eine Endnote. |

## Hinweise


Sowohl Fußnoten als auch Endnoten werden durch Objekte der Klasse [Footnote](./) dargestellt. Verwenden Sie [FootnoteType](../footnote/get_footnotetype/), um zwischen Fußnoten und Endnoten zu unterscheiden.

## Beispiele



Zeigt, wie man Text mit einer Fußnote und einer Endnote referenziert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie etwas Text ein und markieren Sie ihn mit einer Fußnote, wobei die Eigenschaft IsAuto standardmäßig auf "true" gesetzt ist,
// so wird das im Fließtext sichtbare Markierungszeichen automatisch auf "1" nummeriert,
// und die Fußnote erscheint am unteren Rand der Seite.
builder->Write(u"This text will be referenced by a footnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Footnote, u"Footnote comment regarding referenced text.");

// Fügen Sie mehr Text ein und markieren Sie ihn mit einer Endnote mit einem benutzerdefinierten Referenzzeichen,
// das anstelle der Nummer "2" verwendet wird und "IsAuto" auf false gesetzt wird.
builder->Write(u"This text will be referenced by an endnote.");
builder->InsertFootnote(Aspose::Words::Notes::FootnoteType::Endnote, u"Endnote comment regarding referenced text.", u"CustomMark");

// Fußnoten erscheinen immer am unteren Rand des referenzierten Textes,
// so dass dieser Seitenumbruch die Fußnote nicht beeinflusst.
// Andererseits stehen Endnoten immer am Ende des Dokuments
// so dass dieser Seitenumbruch die Endnote auf die nächste Seite verschiebt.
builder->InsertBreak(Aspose::Words::BreakType::PageBreak);

doc->Save(get_ArtifactsDir() + u"DocumentBuilder.InsertFootnote.docx");
```


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

* Namespace [Aspose::Words::Notes](../)
* Library [Aspose.Words for C++](../../)
