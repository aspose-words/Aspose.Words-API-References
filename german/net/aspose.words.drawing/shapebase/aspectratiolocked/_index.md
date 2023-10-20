---
title: ShapeBase.AspectRatioLocked
linktitle: AspectRatioLocked
articleTitle: AspectRatioLocked
second_title: Aspose.Words für .NET
description: ShapeBase AspectRatioLocked eigendom. Gibt an ob das Seitenverhältnis der Form gesperrt ist in C#.
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

Der Standardwert hängt von der ab[`ShapeType`](../../shapetype/) , für dieImage es ist`WAHR` , aber für die anderen Formtypen ist es so`FALSCH`.

Hat nur Auswirkungen auf Formen der obersten Ebene.

## Beispiele

Zeigt, wie das Seitenverhältnis einer Form gesperrt/entsperrt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Eine Form einfügen. Wenn wir dieses Dokument in Microsoft Word öffnen, können wir mit der linken Maustaste auf die Form klicken, um sie anzuzeigen
// acht Größenziehpunkte um den Umfang herum, auf die wir klicken und ziehen können, um die Größe zu ändern.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Setzen Sie die Eigenschaft „AspectRatioLocked“ auf „true“, um das Seitenverhältnis der Form beizubehalten
// wenn Sie einen der vier diagonalen Größenziehpunkte verwenden, die sowohl die Höhe als auch die Breite des Bildes ändern.
// Die Verwendung orthogonaler Größenziehpunkte, die entweder die Höhe oder die Breite ändern, ändert weiterhin das Seitenverhältnis.
// Setzen Sie die Eigenschaft „AspectRatioLocked“ auf „false“, damit wir dies ermöglichen
// Das Seitenverhältnis des Bildes mit allen Größenziehpunkten frei ändern.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
