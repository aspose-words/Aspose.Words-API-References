---
title: ShapeBase.AspectRatioLocked
second_title: Aspose.Words für .NET-API-Referenz
description: ShapeBase eigendom. Gibt an ob das Seitenverhältnis der Form gesperrt ist.
type: docs
weight: 40
url: /de/net/aspose.words.drawing/shapebase/aspectratiolocked/
---
## ShapeBase.AspectRatioLocked property

Gibt an, ob das Seitenverhältnis der Form gesperrt ist.

```csharp
public bool AspectRatioLocked { get; set; }
```

### Bemerkungen

Der Standardwert hängt von der ab[`ShapeType`](../shapetype/) , für das ShapeType.Image ist es **Stimmt** , aber für die anderen Formtypen ist es das **FALSCH**.

Hat nur Auswirkungen auf Formen der obersten Ebene.

### Beispiele

Zeigt, wie das Seitenverhältnis einer Form gesperrt/entsperrt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Form einfügen. Wenn wir dieses Dokument in Microsoft Word öffnen, können wir mit der linken Maustaste auf die Form klicken, um sie anzuzeigen
// acht Ziehpunkte um seinen Umfang herum, die wir anklicken und ziehen können, um seine Größe zu ändern.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");

// Setzen Sie die Eigenschaft "AspectRatioLocked" auf "true", um das Seitenverhältnis der Form beizubehalten
// wenn Sie einen der vier diagonalen Größengriffe verwenden, die sowohl die Höhe als auch die Breite des Bildes ändern.
// Wenn Sie orthogonale Ziehpunkte verwenden, die entweder die Höhe oder Breite ändern, wird das Seitenverhältnis immer noch geändert.
// Setzen Sie die Eigenschaft "AspectRatioLocked" auf "false", um uns dies zu ermöglichen
// das Seitenverhältnis des Bildes mit allen Ziehpunkten frei ändern.
shape.AspectRatioLocked = lockAspectRatio;

doc.Save(ArtifactsDir + "Shape.AspectRatio.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../shapebase/)
* Montage [Aspose.Words](../../../)


