---
title: ShapeBase.CanHaveImage
linktitle: CanHaveImage
articleTitle: CanHaveImage
second_title: Aspose.Words für .NET
description: ShapeBase CanHaveImage eigendom. Gibt zurückWAHR wenn der Formtyp zulässt dass die Form ein Bild hat in C#.
type: docs
weight: 100
url: /de/net/aspose.words.drawing/shapebase/canhaveimage/
---
## ShapeBase.CanHaveImage property

Gibt zurück`WAHR` wenn der Formtyp zulässt, dass die Form ein Bild hat.

```csharp
public bool CanHaveImage { get; }
```

## Bemerkungen

Obwohl Microsoft Word über einen speziellen Formtyp für Bilder verfügt, scheint es, dass in Microsoft Word-Dokumenten jede Form außer einer Gruppenform ein Bild haben kann. Daher wird diese Eigenschaft zurückgegeben`WAHR` für alle Formen außer[`GroupShape`](../../groupshape/).

## Beispiele

Zeigt, wie man ein Bild einfügt und dreht.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Form mit einem Bild einfügen.
Shape shape = builder.InsertImage(Image.FromFile(ImageDir + "Logo.jpg"));
Assert.True(shape.CanHaveImage);
Assert.True(shape.HasImage);

// Das Bild um 45 Grad im Uhrzeigersinn drehen.
shape.Rotation = 45;

doc.Save(ArtifactsDir + "Shape.Rotate.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
