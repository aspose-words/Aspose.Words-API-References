---
title: StoryType Enum
linktitle: StoryType
articleTitle: StoryType
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.StoryType Enumeration und verwalten Sie Textgeschichten in Word-Dokumenten effizient und einfach. Verbessern Sie noch heute Ihre Dokumentverarbeitung!
type: docs
weight: 6970
url: /de/net/aspose.words/storytype/
---
## StoryType enumeration

Der Text eines Word-Dokuments wird in Storys gespeichert.`StoryType` identifiziert eine Geschichte.

```csharp
public enum StoryType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `0` | Standardwert. Es gibt keine solche Story im Dokument. |
| MainText | `1` | Enthält den Haupttext des Dokuments, dargestellt durch[`Body`](../body/) . |
| Footnotes | `2` | Enthält Fußnotentext, dargestellt durch[`Footnote`](../../aspose.words.notes/footnote/) . |
| Endnotes | `3` | Enthält Endnotentext, dargestellt durch[`Footnote`](../../aspose.words.notes/footnote/) . |
| Comments | `4` | Enthält Dokumentkommentare (Annotationen), dargestellt durch[`Comment`](../comment/) . |
| Textbox | `5` | Enthält Form- oder Textfeldtext, dargestellt durch[`Shape`](../../aspose.words.drawing/shape/) . |
| EvenPagesHeader | `6` | Enthält den Text der Kopfzeile der geraden Seiten, dargestellt durch[`HeaderFooter`](../headerfooter/) . |
| PrimaryHeader | `7` | Enthält den Text der primären Kopfzeile. Wenn die Kopfzeile für gerade und ungerade Seiten unterschiedlich ist, enthält den Text der Kopfzeile für ungerade Seiten. Dargestellt durch[`HeaderFooter`](../headerfooter/) . |
| EvenPagesFooter | `8` | Enthält den Text der Fußzeile der geraden Seiten, dargestellt durch[`HeaderFooter`](../headerfooter/) . |
| PrimaryFooter | `9` | Enthält den Text der primären Fußzeile. Wenn die Fußzeile für gerade und ungerade Seiten unterschiedlich ist, enthält den Text der ungeraden Seitenfußzeile. Dargestellt durch[`HeaderFooter`](../headerfooter/) . |
| FirstPageHeader | `10` | Enthält den Text der ersten Seitenüberschrift, dargestellt durch[`HeaderFooter`](../headerfooter/) . |
| FirstPageFooter | `11` | Enthält den Text der Fußzeile der ersten Seite, dargestellt durch[`HeaderFooter`](../headerfooter/) . |
| FootnoteSeparator | `12` | Enthält den Text des Fußnotentrennzeichens. |
| FootnoteContinuationSeparator | `13` | Enthält den Text des Fußnotenfortsetzungstrennzeichens. |
| FootnoteContinuationNotice | `14` | Enthält den Text des Fußnoten-Fortsetzungshinweis-Trennzeichens. |
| EndnoteSeparator | `15` | Enthält den Text des Endnotentrennzeichens. |
| EndnoteContinuationSeparator | `16` | Enthält den Text des Endnoten-Fortsetzungstrennzeichens. |
| EndnoteContinuationNotice | `17` | Enthält den Text des Trennzeichens für den Endnotenfortsetzungshinweis. |

## Beispiele

Zeigt, wie alle Formen aus einem Knoten entfernt werden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Verwenden Sie einen DocumentBuilder, um eine Form einzufügen. Dies ist eine Inline-Form.
// der einen übergeordneten Absatz hat, der ein untergeordneter Knoten des Hauptteils des ersten Abschnitts ist.
builder.InsertShape(ShapeType.Cube, 100.0, 100.0);

Assert.AreEqual(1, doc.GetChildNodes(NodeType.Shape, true).Count);

// Wir können alle Formen aus den untergeordneten Absätzen dieses Textkörpers löschen.
Assert.AreEqual(StoryType.MainText, doc.FirstSection.Body.StoryType);
doc.FirstSection.Body.DeleteShapes();

Assert.AreEqual(0, doc.GetChildNodes(NodeType.Shape, true).Count);
```

### Siehe auch

* namensraum [Aspose.Words](../../aspose.words/)
* Montage [Aspose.Words](../../)
