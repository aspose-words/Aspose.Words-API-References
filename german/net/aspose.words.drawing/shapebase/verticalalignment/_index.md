---
title: ShapeBase.VerticalAlignment
linktitle: VerticalAlignment
articleTitle: VerticalAlignment
second_title: Aspose.Words für .NET
description: ShapeBase VerticalAlignment eigendom. Gibt an wie die Form vertikal positioniert wird in C#.
type: docs
weight: 560
url: /de/net/aspose.words.drawing/shapebase/verticalalignment/
---
## ShapeBase.VerticalAlignment property

Gibt an, wie die Form vertikal positioniert wird.

```csharp
public VerticalAlignment VerticalAlignment { get; set; }
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

* enum [VerticalAlignment](../../verticalalignment/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
