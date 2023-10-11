---
title: Enum WrapType
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Drawing.WrapType opsomming. Gibt an wie Text um eine Form oder ein Bild gewickelt wird.
type: docs
weight: 1400
url: /de/net/aspose.words.drawing/wraptype/
---
## WrapType enumeration

Gibt an, wie Text um eine Form oder ein Bild gewickelt wird.

```csharp
public enum WrapType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| None | `3` | Kein Textumbruch um die Form. Die Form wird hinter oder vor dem Text platziert. |
| Inline | `0` | Die Form bleibt auf derselben Ebene wie der Text und wird als Zeichen behandelt. |
| TopBottom | `1` | Der Text stoppt am oberen Rand der Form und beginnt in der Zeile unterhalb der Form neu. |
| Square | `2` | Wickelt Text um alle Seiten des quadratischen Begrenzungsrahmens der Form. |
| Tight | `4` | Wickelt sich eng um die Kanten der Form, anstatt um den Begrenzungsrahmen. |
| Through | `5` | Wie „Tight“, aber umhüllt alle offenen Teile der Form. |

### Beispiele

Zeigt, wie man ein schwebendes Bild in der Mitte einer Seite einfügt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie ein schwebendes Bild ein, das hinter dem überlappenden Text erscheint, und richten Sie es in der Mitte der Seite aus.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Zeigt, wie man ein Bild einfügt und es als Wasserzeichen verwendet.

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

Zeigt, wie man ein Bild einfügt und es als Wasserzeichen verwendet (.NetStandard 2.0).

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

* property [WrapType](../shapebase/wraptype/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)


