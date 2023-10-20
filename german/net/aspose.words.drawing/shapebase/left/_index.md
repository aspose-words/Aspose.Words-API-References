---
title: ShapeBase.Left
linktitle: Left
articleTitle: Left
second_title: Aspose.Words für .NET
description: ShapeBase Left eigendom. Ruft die Position der linken Kante des enthaltenden Blocks der Form ab oder legt diese fest in C#.
type: docs
weight: 370
url: /de/net/aspose.words.drawing/shapebase/left/
---
## ShapeBase.Left property

Ruft die Position der linken Kante des enthaltenden Blocks der Form ab oder legt diese fest.

```csharp
public double Left { get; set; }
```

## Bemerkungen

Für eine Form der obersten Ebene wird der Wert in Punkten und relativ zum Formanker angegeben.

Für Formen in einer Gruppe liegt der Wert im Koordinatenraum und in den Einheiten der übergeordneten Gruppe.

Der Standardwert ist 0.

Hat nur Auswirkungen auf schwebende Formen.

## Beispiele

Zeigt, wie man ein schwebendes Bild einfügt und seine Position und Größe angibt.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Konfigurieren Sie die Eigenschaft „RelativeHorizontalPosition“ der Form, um den Wert der Eigenschaft „Left“ zu behandeln
 // als horizontaler Abstand der Form in Punkten von der linken Seite der Seite.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Legen Sie den horizontalen Abstand der Form von der linken Seite der Seite auf 100 fest.
shape.Left = 100;

// Verwenden Sie die Eigenschaft „RelativeVerticalPosition“ auf ähnliche Weise, um die Form 80pt unter dem oberen Rand der Seite zu positionieren.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Legen Sie die Höhe der Form fest, wodurch die Breite automatisch skaliert wird, um die Abmessungen beizubehalten.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Die Eigenschaften „Bottom“ und „Right“ enthalten den unteren und rechten Rand des Bildes.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Siehe auch

* class [ShapeBase](../)
* namensraum [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* Montage [Aspose.Words](../../../)
