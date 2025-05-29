---
title: WrapType Enum
linktitle: WrapType
articleTitle: WrapType
second_title: Aspose.Words für .NET
description: Entdecken Sie, wie die Aufzählung Aspose.Words.Drawing.WrapType den Textumbruch um Formen und Bilder für eine professionelle Dokumentformatierung verbessert.
type: docs
weight: 1810
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
| TopBottom | `1` | Der Text endet oben in der Form und beginnt in der Zeile unter der Form neu. |
| Square | `2` | Umschließt alle Seiten des quadratischen Begrenzungsrahmens der Form mit Text. |
| Tight | `4` | Schließt sich eng um die Kanten der Form, anstatt um den Begrenzungsrahmen. |
| Through | `5` | Dasselbe wie „Tight“, wickelt sich aber in alle offenen Teile der Form ein. |

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

* property [WrapType](../shapebase/wraptype/)
* namensraum [Aspose.Words.Drawing](../../aspose.words.drawing/)
* Montage [Aspose.Words](../../)
