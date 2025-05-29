---
title: DocumentDirection Enum
linktitle: DocumentDirection
articleTitle: DocumentDirection
second_title: Aspose.Words für .NET
description: Entdecken Sie die Enumeration Aspose.Words.DocumentDirection, um den Textfluss in Ihren Dokumenten einfach zu steuern. Verbessern Sie Lesbarkeit und Formatierung mit dieser leistungsstarken Funktion!
type: docs
weight: 4030
url: /de/net/aspose.words.loading/documentdirection/
---
## DocumentDirection enumeration

Ermöglicht die Angabe der Textflussrichtung in einem Dokument.

```csharp
public enum DocumentDirection
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| LeftToRight | `0` | Von links nach rechts. |
| RightToLeft | `1` | Von rechts nach links. |
| Auto | `2` | Richtung automatisch erkennen. |

## Beispiele

Zeigt, wie die Textrichtung in Klartextdokumenten erkannt wird.

```csharp
// Erstelle ein "TxtLoadOptions"-Objekt, das wir an den Konstruktor eines Dokuments übergeben können
// um zu ändern, wie wir ein Klartextdokument laden.
TxtLoadOptions loadOptions = new TxtLoadOptions();

// Setzen Sie die Eigenschaft "DocumentDirection" auf "DocumentDirection.Auto" erkennt automatisch
// die Richtung jedes Textabsatzes, den Aspose.Words aus dem Klartext lädt.
// Die „Bidi“-Eigenschaft jedes Absatzes speichert seine Richtung.
loadOptions.DocumentDirection = DocumentDirection.Auto;

// Hebräischen Text als von rechts nach links lesend erkennen.
Document doc = new Document(MyDir + "Hebrew text.txt", loadOptions);

Assert.True(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);

// Englischen Text als von rechts nach links lesend erkennen.
doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.False(doc.FirstSection.Body.FirstParagraph.ParagraphFormat.Bidi);
```

### Siehe auch

* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
