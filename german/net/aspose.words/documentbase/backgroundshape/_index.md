---
title: DocumentBase.BackgroundShape
linktitle: BackgroundShape
articleTitle: BackgroundShape
second_title: Aspose.Words für .NET
description: Entdecken Sie die DocumentBase BackgroundShape-Eigenschaft und passen Sie die Hintergrundform Ihres Dokuments ganz einfach an, um die Optik zu verbessern. Maximieren Sie Ihr Designpotenzial!
type: docs
weight: 10
url: /de/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

Ruft die Hintergrundform des Dokuments ab oder legt sie fest. Kann sein`null` .

```csharp
public Shape BackgroundShape { get; set; }
```

## Bemerkungen

Microsoft Word erlaubt nur eine Form, die ihre[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) Eigenschaft equal zuRectangle zur Verwendung als Hintergrundform für ein Dokument.

Microsoft Word unterstützt nur die Fülleigenschaften einer Hintergrundform. Alle anderen Eigenschaften werden ignoriert.

Wenn Sie diese Eigenschaft auf einen Wert ungleich Null setzen, wird auch die[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) Zu`WAHR`.

## Beispiele

Zeigt, wie für jede Seite eines Dokuments eine Hintergrundform festgelegt wird.

```csharp
Document doc = new Document();

Assert.IsNull(doc.BackgroundShape);

// Der einzige Formtyp, den wir als Hintergrund verwenden können, ist ein Rechteck.
Shape shapeRectangle = new Shape(doc, ShapeType.Rectangle);

// Es gibt zwei Möglichkeiten, diese Form als Seitenhintergrund zu verwenden.
// 1 - Eine flache Farbe:
shapeRectangle.FillColor = System.Drawing.Color.LightBlue;
doc.BackgroundShape = shapeRectangle;

doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.FlatColor.docx");

// 2 - Ein Bild:
shapeRectangle = new Shape(doc, ShapeType.Rectangle);
shapeRectangle.ImageData.SetImage(ImageDir + "Transparent background logo.png");

// Passen Sie das Erscheinungsbild des Bildes an, um es besser als Wasserzeichen geeignet zu machen.
shapeRectangle.ImageData.Contrast = 0.2;
shapeRectangle.ImageData.Brightness = 0.7;

doc.BackgroundShape = shapeRectangle;

Assert.IsTrue(doc.BackgroundShape.HasImage);

Aspose.Words.Saving.PdfSaveOptions saveOptions = new Aspose.Words.Saving.PdfSaveOptions
{
    CacheBackgroundGraphics = false
};

// Microsoft Word unterstützt keine Formen mit Bildern als Hintergrund,
// aber wir können diese Hintergründe immer noch in anderen Speicherformaten wie .pdf sehen.
doc.Save(ArtifactsDir + "DocumentBase.BackgroundShape.Image.pdf", saveOptions);
```

### Siehe auch

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBase](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
