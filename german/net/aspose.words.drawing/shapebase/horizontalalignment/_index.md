---
title: ShapeBase.HorizontalAlignment
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase HorizontalAlignment-Eigenschaft, um die horizontale Positionierung von Formen in Ihrem Design für eine verbesserte Layoutkontrolle zu optimieren.
type: docs
weight: 240
url: /de/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

Gibt an, wie die Form horizontal positioniert wird.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

## Bemerkungen

Der Standardwert istNone.

Wirkt sich nur auf schwebende Formen der obersten Ebene aus.

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

### Siehe auch

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
