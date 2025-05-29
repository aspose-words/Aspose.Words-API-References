---
title: ShapeBase.BehindText
linktitle: BehindText
articleTitle: BehindText
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase-Eigenschaft „BehindText“, um die Formschichtung in Ihren Designs zu steuern und so mühelos die Textsichtbarkeit und Layoutpräzision zu verbessern.
type: docs
weight: 50
url: /de/net/aspose.words.drawing/shapebase/behindtext/
---
## ShapeBase.BehindText property

Gibt an, ob sich die Form unter oder über dem Text befindet.

```csharp
public bool BehindText { get; set; }
```

## Bemerkungen

Wirkt sich nur auf Formen der obersten Ebene aus.

Der Standardwert ist`FALSCH`.

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

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
