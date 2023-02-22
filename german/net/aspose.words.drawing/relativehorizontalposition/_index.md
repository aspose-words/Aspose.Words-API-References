---
title: Enum RelativeHorizontalPosition
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.RelativeHorizontalPosition opsomming. Gibt an zu welcher horizontalen Position eine Form oder ein Textrahmen relativ ist.
type: docs
weight: 1060
url: /de/net/aspose.words.drawing/relativehorizontalposition/
---
## RelativeHorizontalPosition enumeration

Gibt an, zu welcher horizontalen Position eine Form oder ein Textrahmen relativ ist.

```csharp
public enum RelativeHorizontalPosition
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| Margin | `0` | Gibt an, dass die horizontale Positionierung relativ zu den Seitenrändern erfolgen soll. |
| Page | `1` | Das Objekt wird relativ zum linken Rand der Seite positioniert. |
| Column | `2` | Das Objekt wird relativ zur linken Seite der Spalte positioniert. |
| Character | `3` | Das Objekt wird relativ zur linken Seite des Absatzes positioniert. |
| LeftMargin | `4` | Gibt an, dass die horizontale Positionierung relativ zum linken Rand der Seite erfolgen soll. |
| RightMargin | `5` | Gibt an, dass die horizontale Positionierung relativ zum rechten Rand der Seite erfolgen soll. |
| InsideMargin | `6` | Gibt an, dass die horizontale Positionierung relativ zum Innenrand der aktuellen Seite sein soll (der linke Rand auf ungeraden Seiten, rechts auf geraden Seiten). |
| OutsideMargin | `7` | Gibt an, dass die horizontale Positionierung relativ zum Außenrand der aktuellen Seite sein soll (der rechte Rand auf ungeraden Seiten, der linke auf geraden Seiten). |
| Default | `2` | Standardwert istColumn . |

### Beispiele

Zeigt, wie ein schwebendes Bild in der Mitte einer Seite eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text angezeigt wird, und richten Sie es an der Mitte der Seite aus.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Zeigt, wie ein Bild eingefügt und als Wasserzeichen verwendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie das Bild in die Kopfzeile ein, damit es auf jeder Seite sichtbar ist.
Image image = Image.FromFile(ImageDir + "Transparent background logo.png");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(image);
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Platzieren Sie das Bild in der Mitte der Seite.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Zeigt, wie ein Bild eingefügt und als Wasserzeichen verwendet wird (.NetStandard 2.0).

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie das Bild in die Kopfzeile ein, damit es auf jeder Seite sichtbar ist.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);

using (SKBitmap image = SKBitmap.Decode(ImageDir + "Transparent background logo.png"))
{
    builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
    Shape shape = builder.InsertImage(image);
    shape.WrapType = WrapType.None;
    shape.BehindText = true;

    // Platzieren Sie das Bild in der Mitte der Seite.
    shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
    shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
    shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
    shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;
}

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermarkNetStandard2.docx");
```

### Siehe auch

* property [RelativeHorizontalPosition](../shapebase/relativehorizontalposition/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


