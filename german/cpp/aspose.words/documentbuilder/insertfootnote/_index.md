---
title: "Aspose::Words::DocumentBuilder::InsertFootnote Methode"
linktitle: "InsertFootnote"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::DocumentBuilder::InsertFootnote Methode. Fügt eine Fußnote oder Endnote in das Dokument in C++ ein."
type: docs
weight: 35000
url: /de/cpp/aspose.words/documentbuilder/insertfootnote/
---
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&) method


Fügt eine Fußnote oder Endnote in das Dokument ein.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Gibt an, ob eine Fußnote oder eine Endnote eingefügt werden soll. |
| footnoteText | const System::String\& | Gibt den Text der Fußnote an. |

### ReturnValue

Gibt ein Fußnotenobjekt zurück, das gerade erstellt wurde.

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

## Siehe auch

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
## DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType, const System::String\&, const System::String\&) method


Fügt eine Fußnote oder Endnote in das Dokument ein.

```cpp
System::SharedPtr<Aspose::Words::Notes::Footnote> Aspose::Words::DocumentBuilder::InsertFootnote(Aspose::Words::Notes::FootnoteType footnoteType, const System::String &footnoteText, const System::String &referenceMark)
```


| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| footnoteType | Aspose::Words::Notes::FootnoteType | Gibt an, ob eine Fußnote oder eine Endnote eingefügt werden soll. |
| footnoteText | const System::String\& | Gibt den Text der Fußnote an. |
| referenceMark | const System::String\& | Gibt das benutzerdefinierte Referenzzeichen der Fußnote an. |

### ReturnValue

Gibt ein Fußnotenobjekt zurück, das gerade erstellt wurde.

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

## Siehe auch

* Class [Footnote](../../../aspose.words.notes/footnote/)
* Enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* Class [DocumentBuilder](../)
* Namespace [Aspose::Words](../../)
* Library [Aspose.Words for C++](../../../)
