---
title: ShapeBase.RelativeVerticalPosition
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Gibt relativ zur vertikalen Positionierung der Form an.
type: docs
weight: 440
url: /de/net/aspose.words.drawing/shapebase/relativeverticalposition/
---
## ShapeBase.RelativeVerticalPosition property

Gibt relativ zur vertikalen Positionierung der Form an.

```csharp
public RelativeVerticalPosition RelativeVerticalPosition { get; set; }
```

### Bemerkungen

Der Standardwert istParagraph.

Hat nur Auswirkungen auf schwebende Formen der obersten Ebene.

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

### Siehe auch

* enum [RelativeVerticalPosition](../../relativeverticalposition/)
* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


