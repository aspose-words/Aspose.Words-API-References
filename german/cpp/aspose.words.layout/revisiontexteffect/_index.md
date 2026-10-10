---
title: "Aspose::Words::Layout::RevisionTextEffect Enum"
linktitle: "RevisionTextEffect"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::RevisionTextEffect Enum. Ermöglicht die Angabe des Dekorationseffekts für Revisionen von Dokumenttext in C++."
type: docs
weight: 12000
url: /de/cpp/aspose.words.layout/revisiontexteffect/
---
## RevisionTextEffect enum


Ermöglicht die Angabe eines Dekorationseffekts für Revisionen von Dokumenttext.

```cpp
enum class RevisionTextEffect
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | 0 | Überarbeiteter Inhalt hat keine speziellen Effekte angewendet. Dies entspricht [NoHighlight](../revisioncolor/). |
| Farbe | 1 | Überarbeiteter Inhalt wird nur mit Farbe hervorgehoben. |
| Bold | 2 | Überarbeiteter Inhalt wird fett und farbig dargestellt. |
| Kursiv | 3 | Überarbeiteter Inhalt wird kursiv und farbig dargestellt. |
| Underline | 4 | Überarbeiteter Inhalt wird unterstrichen und farbig dargestellt. |
| DoubleUnderline | 5 | Überarbeiteter Inhalt wird doppelt unterstrichen und farbig dargestellt. |
| StrikeThrough | 6 | Überarbeiteter Inhalt wird durchgestrichen und farbig dargestellt. |
| DoubleStrikeThrough | 7 | Überarbeiteter Inhalt wird doppelt durchgestrichen und farbig dargestellt. |
| Hidden | 8 | Überarbeiteter Inhalt ist ausgeblendet. |


## Beispiele



Zeigt, wie das Erscheinungsbild von Revisionen geändert wird.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Revisions.docx");

// Holen Sie das RevisionOptions-Objekt, das das Erscheinungsbild von Revisionen steuert.
System::SharedPtr<Aspose::Words::Layout::RevisionOptions> revisionOptions = doc->get_LayoutOptions()->get_RevisionOptions();

// Rendern Sie Einfüge-Revisionen in Grün und kursiv.
revisionOptions->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::Green);
revisionOptions->set_InsertedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Italic);

// Rendern Sie Lösch-Revisionen in Rot und fett.
revisionOptions->set_DeletedTextColor(Aspose::Words::Layout::RevisionColor::Red);
revisionOptions->set_DeletedTextEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Der gleiche Text erscheint zweimal in einer Bewegungs-Revision:
// einmal am Abfahrtspunkt und einmal am Ankunftsziel.
// Rendern Sie den Text bei der verschobenen‑von‑Revision gelb mit einem doppelten Durchstreichen
// und doppelt unterstrichen blau bei der verschobenen‑zu‑Revision.
revisionOptions->set_MovedFromTextColor(Aspose::Words::Layout::RevisionColor::Yellow);
revisionOptions->set_MovedFromTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleStrikeThrough);
revisionOptions->set_MovedToTextColor(Aspose::Words::Layout::RevisionColor::ClassicBlue);
revisionOptions->set_MovedToTextEffect(Aspose::Words::Layout::RevisionTextEffect::DoubleUnderline);

// Rendern Sie Formatrevisionen in dunklem Rot und fett.
revisionOptions->set_RevisedPropertiesColor(Aspose::Words::Layout::RevisionColor::DarkRed);
revisionOptions->set_RevisedPropertiesEffect(Aspose::Words::Layout::RevisionTextEffect::Bold);

// Platzieren Sie einen dicken dunkelblauen Balken auf der linken Seite der Seite neben den von Revisionen betroffenen Zeilen.
revisionOptions->set_RevisionBarsColor(Aspose::Words::Layout::RevisionColor::DarkBlue);
revisionOptions->set_RevisionBarsWidth(15.0f);

// Zeigen Sie Revisionsmarkierungen und den Originaltext.
revisionOptions->set_ShowOriginalRevision(true);
revisionOptions->set_ShowRevisionMarks(true);

// Lassen Sie Bewegungs-, Lösch‑, Formatierungsrevisionen und Kommentare in grünen Sprechblasen erscheinen
// auf der rechten Seite der Seite.
revisionOptions->set_ShowInBalloons(Aspose::Words::Layout::ShowInBalloons::Format);
revisionOptions->set_CommentColor(Aspose::Words::Layout::RevisionColor::BrightGreen);

// Diese Funktionen gelten nur für Formate wie .pdf oder .jpg.
doc->Save(get_ArtifactsDir() + u"Revision.RevisionOptions.pdf");
```

## Siehe auch

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
