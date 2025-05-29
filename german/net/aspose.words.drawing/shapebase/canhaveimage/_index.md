---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase CanHaveImage-Eigenschaft – erfahren Sie, wie Sie feststellen, ob Ihr Formtyp Bilder für eine verbesserte visuelle Attraktivität unterstützt!
type: docs
weight: 100
url: /de/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

Rückgaben`WAHR` wenn der Formtyp es zulässt, dass die Form ein Bild enthält.

```csharp
public bool CanHaveImage { get; }
```

## Bemerkungen

Obwohl Microsoft Word einen speziellen Formtyp für Bilder hat, scheint es, dass in Microsoft Word-Dokumenten jede Form außer einer Gruppenform ein Bild haben kann, daher gibt diese Eigenschaft zurück`WAHR` für alle Formen außer[`GroupShape`](../../groupshape/).

## Beispiele

Zeigt, wie man ein Bild einfügt und dreht.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Form mit einem Bild ein.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Drehen Sie das Bild um 45 Grad im Uhrzeigersinn.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
