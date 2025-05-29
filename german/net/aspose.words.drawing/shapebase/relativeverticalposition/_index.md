---
title: ShapeBase.RelativeVerticalPosition
linktitle: RelativeVerticalPosition
articleTitle: RelativeVerticalPosition
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase-Eigenschaft „RelativeVerticalPosition“, um die vertikale Ausrichtung von Formen zu verbessern und so eine präzise Layoutkontrolle in Ihren Designs sicherzustellen.
type: docs
weight: 470
url: /de/net/aspose.words.drawing/shapebase/relativeverticalposition/
---
## ShapeBase.RelativeVerticalPosition property

Gibt an, relativ zu welcher vertikalen Position die Form positioniert ist.

```csharp
public RelativeVerticalPosition RelativeVerticalPosition { get; set; }
```

## Bemerkungen

Der Standardwert istParagraph.

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

* enum [RelativeVerticalPosition](../../relativeverticalposition/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
