---
title: ShapeBase.BehindText
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Gibt an ob die Form unter oder über dem Text liegt.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

Gibt an, ob die Form unter oder über dem Text liegt.

```csharp
public bool BehindText { get; set; }
```

### Bemerkungen

Hat nur Auswirkungen auf Formen der obersten Ebene.

Der Standardwert ist`FALSCH`.

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

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


