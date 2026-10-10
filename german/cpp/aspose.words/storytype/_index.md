---
title: "Aspose::Words::StoryType enum"
linktitle: "StoryType"
second_title: "Aspose.Words für C++ API‑Referenz"
description: "Aspose::Words::StoryType enum. Der Text eines Word-Dokuments wird in Stories gespeichert. StoryType identifiziert eine Story in C++."
type: docs
weight: 117000
url: /de/cpp/aspose.words/storytype/
---
## StoryType enum


Der Text eines Word-Dokuments wird in Stories gespeichert. [StoryType](./) identifiziert eine Story.

```cpp
enum class StoryType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Keine | 0 | Standardwert. Es gibt keine solche Story im Dokument. |
| MainText | 1 | Enthält den Haupttext des Dokuments, dargestellt durch [Body](../body/). |
| Footnotes | 2 | Enthält Fußnotentext, dargestellt durch [Footnote](../../aspose.words.notes/footnote/). |
| Endnotes | 3 | Enthält Endnotentext, dargestellt durch [Footnote](../../aspose.words.notes/footnote/). |
| Comments | 4 | Enthält Dokumentkommentare (Anmerkungen), dargestellt durch [Comment](../comment/). |
| Textbox | 5 | Enthält Text von Formen oder Textfeldern, dargestellt durch [Shape](../../aspose.words.drawing/shape/). |
| EvenPagesHeader | 6 | Enthält den Text der Kopfzeile für gerade Seiten, dargestellt durch [HeaderFooter](../headerfooter/). |
| PrimaryHeader | 7 | Enthält den Text der primären Kopfzeile. Wenn die Kopfzeile für ungerade und gerade Seiten unterschiedlich ist, enthält sie den Text der Kopfzeile für ungerade Seiten. Darstellung erfolgt durch [HeaderFooter](../headerfooter/). |
| EvenPagesFooter | 8 | Enthält den Text der Fußzeile der geraden Seiten, dargestellt durch [HeaderFooter](../headerfooter/). |
| PrimaryFooter | 9 | Enthält den Text der primären Fußzeile. Wenn die Fußzeile für ungerade und gerade Seiten unterschiedlich ist, enthält sie den Text der Fußzeile der ungeraden Seiten. Darstellung erfolgt durch [HeaderFooter](../headerfooter/). |
| FirstPageHeader | 10 | Enthält den Text der Kopfzeile der ersten Seite, dargestellt durch [HeaderFooter](../headerfooter/). |
| FirstPageFooter | 11 | Enthält den Text der Fußzeile der ersten Seite, dargestellt durch [HeaderFooter](../headerfooter/). |
| FootnoteSeparator | 12 | Enthält den Text des Fußnotentrennzeichens. |
| FootnoteContinuationSeparator | 13 | Enthält den Text des Fortsetzungs‑Trennzeichens für Fußnoten. |
| FootnoteContinuationNotice | 14 | Enthält den Text des Trennzeichens für die Fortsetzungsmitteilung von Fußnoten. |
| EndnoteSeparator | 15 | Enthält den Text des Endnotentrennzeichens. |
| EndnoteContinuationSeparator | 16 | Enthält den Text des Fortsetzungs‑Trennzeichens für Endnoten. |
| EndnoteContinuationNotice | 17 | Enthält den Text des Trennzeichens für die Fortsetzungsmitteilung von Endnoten. |


## Beispiele



Zeigt, wie man alle Formen aus einem Knoten entfernt.
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
auto builder = System::MakeObject<Aspose::Words::DocumentBuilder>(doc);

// Verwenden Sie einen DocumentBuilder, um eine Form einzufügen. Dies ist eine Inline-Form,
// die einen übergeordneten Absatz hat, der ein Kindknoten des Body der ersten Abschnitts ist.
builder->InsertShape(Aspose::Words::Drawing::ShapeType::Cube, 100.0, 100.0);

ASSERT_EQ(1, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());

// Wir können alle Formen aus den Kindabsätzen dieses Body löschen.
ASSERT_EQ(Aspose::Words::StoryType::MainText, doc->get_FirstSection()->get_Body()->get_StoryType());
doc->get_FirstSection()->get_Body()->DeleteShapes();

ASSERT_EQ(0, doc->GetChildNodes(Aspose::Words::NodeType::Shape, true)->get_Count());
```

## Siehe auch

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
