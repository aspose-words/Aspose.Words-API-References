---
title: ShapeBase.HorizontalAlignment
linktitle: HorizontalAlignment
articleTitle: HorizontalAlignment
second_title: Aspose.Words für .NET
description: ShapeBase HorizontalAlignment eigendom. Gibt an wie die Form horizontal positioniert wird in C#.
type: docs
weight: 220
url: /de/net/aspose.words.drawing/shapebase/horizontalalignment/
---
## ShapeBase.HorizontalAlignment property

Gibt an, wie die Form horizontal positioniert wird.

```csharp
public HorizontalAlignment HorizontalAlignment { get; set; }
```

## Bemerkungen

Der Standardwert istNone.

Hat nur Auswirkungen auf schwebende Formen der obersten Ebene.

## Beispiele

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

### Siehe auch

* enum [HorizontalAlignment](../../horizontalalignment/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
