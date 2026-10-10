---
title: "Aspose::Words::Layout::RevisionColor Enum"
linktitle: "RevisionColor"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::Layout::RevisionColor‑Enum. Ermöglicht die Angabe der Farbe von Dokumentrevisionen in C++."
type: docs
weight: 11000
url: /de/cpp/aspose.words.layout/revisioncolor/
---
## RevisionColor enum


Ermöglicht die Angabe der Farbe von Dokumentrevisionen.

```cpp
enum class RevisionColor
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Auto | 0 | Standard. |
| Schwarz | 1 | Stellt die Farbe 000000 dar. |
| Blau | 2 | Stellt die Farbe 2e97d3 dar. |
| BrightGreen | 3 | Stellt die Farbe 84a35b dar. |
| ClassicBlue | 4 | Stellt die Farbe 0000ff dar. |
| ClassicRed | 5 | Stellt die Farbe ff0000 dar. |
| DarkBlue | 6 | Stellt die Farbe 376e96 dar. |
| DarkRed | 7 | Stellt die Farbe 881824 dar. |
| DarkYellow | 8 | Stellt die Farbe e09a2b dar. |
| Gray25 | 9 | Stellt die Farbe a0a3a9 dar. |
| Gray50 | 10 | Stellt die Farbe 50565e dar. |
| Green | 11 | Stellt die Farbe 2c6234 dar. |
| Pink | 12 | Stellt die Farbe ce338f dar. |
| Red | 13 | Stellt die Farbe b5082e dar. |
| Teal | 14 | Stellt die Farbe 1b9cab dar. |
| Turquoise | 15 | Stellt die Farbe 3eafc2 dar. |
| Violet | 16 | Stellt die Farbe 633277 dar. |
| White | 17 | Stellt die Farbe ffffff dar. |
| Gelb | 18 | Stellt die Farbe fad272 dar. |
| Hellrosa | 19 | Stellt die Farbe fce6f4 dar. |
| Hellblau | 20 | Stellt die Farbe e1f2fa dar. |
| Hellgelb | 21 | Stellt die Farbe fef4de dar. |
| Hellviolett | 22 | Stellt die Farbe eadfef dar. |
| Hellorange | 23 | Stellt die Farbe fce3d0 dar. |
| Hellgrün | 24 | Stellt die Farbe e9f8ce dar. |
| Grau | 25 | Stellt die Farbe efeded dar. |
| NoHighlight | 26 | Es wird keine Farbe verwendet, um Änderungen der Revision hervorzuheben. |
| ByAuthor | 27 | Revisionen jedes Autors erhalten ihre eigene Farbe zur Hervorhebung aus einem vordefinierten Satz hochkontrastierender Farben. |


## Beispiele



Zeigt, wie man das Aussehen von Revisionen in einem gerenderten Ausgabedokument ändert.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Fügen Sie eine Revision ein und ändern Sie dann die Farbe aller Revisionen zu Grün.
builder->Writeln(u"This is not a revision.");
doc->StartTrackRevisions(u"John Doe", System::DateTime::get_Now());
builder->Writeln(u"This is a revision.");
doc->StopTrackRevisions();
builder->Writeln(u"This is not a revision.");

// Entfernen Sie die Leiste, die links von jeder überarbeiteten Zeile erscheint.
doc->get_LayoutOptions()->get_RevisionOptions()->set_InsertedTextColor(Aspose::Words::Layout::RevisionColor::BrightGreen);
doc->get_LayoutOptions()->get_RevisionOptions()->set_ShowRevisionBars(false);
doc->get_LayoutOptions()->get_RevisionOptions()->set_RevisionBarsPosition(Aspose::Words::Drawing::HorizontalAlignment::Right);

doc->Save(get_ArtifactsDir() + u"Revision.LayoutOptionsRevisions.pdf");
```

## Siehe auch

* Namespace [Aspose::Words::Layout](../)
* Library [Aspose.Words for C++](../../)
