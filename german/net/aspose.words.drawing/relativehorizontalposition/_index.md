---
title: RelativeHorizontalPosition Enum
linktitle: RelativeHorizontalPosition
articleTitle: RelativeHorizontalPosition
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.Drawing.RelativeHorizontalPosition, um die präzise horizontale Positionierung für Formen und Textrahmen in Ihren Dokumenten zu definieren.
type: docs
weight: 1580
url: /de/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

Gibt an, worauf sich die horizontale Position einer Form oder eines Textrahmens bezieht.

```csharp
public enum RelativeHorizontalPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Margin | `0` | Gibt an, dass die horizontale Positionierung relativ zu den Seitenrändern erfolgen soll. |
| Page | `1` | Das Objekt wird relativ zum linken Seitenrand positioniert. |
| Column | `2` | Das Objekt wird relativ zur linken Seite der Spalte positioniert. |
| Character | `3` | Das Objekt wird relativ zur linken Seite des Absatzes positioniert. |
| LeftMargin | `4` | Gibt an, dass die horizontale Positionierung relativ zum linken Seitenrand erfolgen soll. |
| RightMargin | `5` | Gibt an, dass die horizontale Positionierung relativ zum rechten Seitenrand erfolgen soll. |
| InsideMargin | `6` | Gibt an, dass die horizontale Positionierung relativ zum Innenrand der aktuellen Seite erfolgen soll (der linke Rand auf ungeraden Seiten, der rechte auf geraden Seiten). |
| OutsideMargin | `7` | Gibt an, dass die horizontale Positionierung relativ zum äußeren Rand der aktuellen Seite erfolgen soll (der rechte Rand auf ungeraden Seiten, der linke auf geraden Seiten). |
| Default | `2` | Der Standardwert istColumn . |

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

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
