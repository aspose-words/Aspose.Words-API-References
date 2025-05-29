---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words für .NET
description: Entdecken Sie die ShapeBase AspectRatioLocked-Eigenschaft, um das Seitenverhältnis Ihrer Formen mühelos beizubehalten und perfekte Designs zu erzielen. Optimieren Sie Ihre Projekte noch heute!
type: docs
weight: 40
url: /de/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

Gibt an, ob das Seitenverhältnis der Form gesperrt ist.

```csharp
public bool AspectRatioLocked { get; set; }
```

## Bemerkungen

Der Standardwert hängt von der[`ShapeType`](../../shapetype/) für dieImage es ist`WAHR` aber für die anderen Formtypen ist es`FALSCH`.

Wirkt sich nur auf Formen der obersten Ebene aus.

## Beispiele

Zeigt, wie das Seitenverhältnis einer Form gesperrt/entsperrt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie eine Form ein. Wenn wir dieses Dokument in Microsoft Word öffnen, können wir mit der linken Maustaste auf die Form klicken, um
// acht Größenziehpunkte um den Umfang, die wir anklicken und ziehen können, um die Größe zu ändern.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Setzen Sie die Eigenschaft „AspectRatioLocked“ auf „true“, um das Seitenverhältnis der Form beizubehalten
// wenn Sie einen der vier diagonalen Größengriffe verwenden, die sowohl die Höhe als auch die Breite des Bildes ändern.
// Die Verwendung orthogonaler Größengriffe, die entweder die Höhe oder die Breite ändern, ändert weiterhin das Seitenverhältnis.
// Setzen Sie die Eigenschaft "AspectRatioLocked" auf "false", um uns zu ermöglichen
// Ändern Sie das Seitenverhältnis des Bildes mit allen Größengriffen frei.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
