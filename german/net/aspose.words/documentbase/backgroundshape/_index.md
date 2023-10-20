---
title: DocumentBase.BackgroundShape
linktitle: BackgroundShape
articleTitle: BackgroundShape
second_title: Aspose.Words für .NET
description: DocumentBase BackgroundShape eigendom. Ruft die Hintergrundform des Dokuments ab oder legt diese fest. Kann seinNull  in C#.
type: docs
weight: 10
url: /de/net/aspose.words/documentbase/backgroundshape/
---
## DocumentBase.BackgroundShape property

Ruft die Hintergrundform des Dokuments ab oder legt diese fest. Kann sein`Null` .

```csharp
public Shape BackgroundShape { get; set; }
```

## Bemerkungen

Microsoft Word erlaubt nur eine Form, die ihre eigenen hat[`ShapeType`](../../../aspose.words.drawing/shapebase/shapetype/) Eigenschaft equal toRectangle als Hintergrundform für ein Dokument verwendet werden.

Microsoft Word unterstützt nur die Fülleigenschaften einer Hintergrundform. Alle anderen Properties werden ignoriert.

Wenn Sie diese Eigenschaft auf einen Wert ungleich Null setzen, wird auch die festgelegt[`DisplayBackgroundShape`](../../../aspose.words.settings/viewoptions/displaybackgroundshape/) Zu`WAHR`.

## Beispiele

Zeigt, wie man für jede Seite eines Dokuments eine Hintergrundform festlegt.

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

// Passen Sie das Erscheinungsbild des Bildes an, damit es besser als Wasserzeichen geeignet ist.
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
