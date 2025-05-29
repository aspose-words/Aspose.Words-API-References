---
title: RelativeVerticalPosition Enum
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.RelativeVerticalPosition, um die vertikale Positionierung von Formen und Textrahmen effektiv zu definieren und Dokumentlayouts zu verbessern.
type: docs
weight: 1600
url: /de/net/aspose.words.drawing/relativeverticalposition/
---
## RelativeVerticalPosition enumeration

Gibt an, worauf sich die vertikale Position einer Form oder eines Textrahmens bezieht.

```csharp
public enum RelativeVerticalPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Margin | `0` | Gibt an, dass die vertikale Positionierung relativ zu den Seitenrändern erfolgen soll. |
| Page | `1` | Das Objekt wird relativ zum oberen Seitenrand positioniert. |
| Paragraph | `2` | Das Objekt wird relativ zum oberen Rand des Absatzes positioniert, der den Anker enthält. |
| Line | `3` | Ohne Papiere. |
| TopMargin | `4` | Gibt an, dass die vertikale Positionierung relativ zum oberen Rand der aktuellen Seite erfolgen soll. |
| BottomMargin | `5` | Gibt an, dass die vertikale Positionierung relativ zum unteren Rand der aktuellen Seite erfolgen soll. |
| InsideMargin | `6` | Gibt an, dass die vertikale Positionierung relativ zum Innenrand der aktuellen Seite erfolgen soll. |
| OutsideMargin | `7` | Gibt an, dass die vertikale Positionierung relativ zum äußeren Rand der aktuellen Seite erfolgen soll. |
| TableDefault | `0` | Der Standardwert istMargin. |
| TextFrameDefault | `2` | Der Standardwert istParagraph. |

## Beispiele

Zeigt, wie ein schwebendes Bild in die Mitte einer Seite eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text angezeigt wird, und richten Sie es an der Seitenmitte aus.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Zeigt, wie Sie ein Bild einfügen und als Wasserzeichen verwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie das Bild in die Kopfzeile ein, damit es auf jeder Seite sichtbar ist.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Platzieren Sie das Bild in der Mitte der Seite.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

### Siehe auch

* property [RelativeVerticalPosition](../shapebase/relativeverticalposition/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
