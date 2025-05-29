---
title: PageSetup.PageWidth
linktitle: PageWidth
articleTitle: PageWidth
second_title: Aspose.Words für .NET
description: Entdecken Sie die PageSetup PageWidth-Eigenschaft, um die Seitenbreite einfach in Punkten anzupassen und so das Layout Ihres Dokuments für eine optimale Präsentation zu verbessern.
type: docs
weight: 340
url: /de/net/aspose.words/pagesetup/pagewidth/
---
## PageSetup.PageWidth property

Gibt die Breite der Seite in Punkten zurück oder legt sie fest.

```csharp
public double PageWidth { get; set; }
```

## Beispiele

Zeigt, wie Sie ein Bild einfügen und als Wasserzeichen verwenden.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Fügen Sie das Bild in die Kopfzeile ein, damit es auf jeder Seite sichtbar ist.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
Shape shape = builder.InsertImage(ImageDir + "Transparent background logo.png");
shape.WrapType = WrapType.None;
shape.BehindText = true;

// Platzieren Sie das Bild in der Mitte der Seite.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Left = (builder.PageSetup.PageWidth - shape.Width) / 2;
shape.Top = (builder.PageSetup.PageHeight - shape.Height) / 2;

doc.Save(ArtifactsDir + "DocumentBuilder.InsertWatermark.docx");
```

Zeigt, wie Sie ein schwebendes Bild einfügen und seine Position und Größe angeben.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;

// Konfigurieren Sie die Eigenschaft „RelativeHorizontalPosition“ der Form, um den Wert der Eigenschaft „Left“ zu behandeln
    // als horizontaler Abstand der Form in Punkten von der linken Seite der Seite.
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;

// Setzen Sie den horizontalen Abstand der Form von der linken Seite der Seite auf 100.
shape.Left = 100;

// Verwenden Sie die Eigenschaft „RelativeVerticalPosition“ auf ähnliche Weise, um die Form 80pt unterhalb des oberen Seitenrands zu positionieren.
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.Top = 80;

// Legen Sie die Höhe der Form fest. Dadurch wird die Breite automatisch skaliert, um die Abmessungen beizubehalten.
shape.Height = 125;

Assert.AreEqual(125.0d, shape.Width);

// Die Eigenschaften „Bottom“ und „Right“ enthalten die unteren und rechten Ränder des Bildes.
Assert.AreEqual(shape.Top + shape.Height, shape.Bottom);
Assert.AreEqual(shape.Left + shape.Width, shape.Right);

doc.Save(ArtifactsDir + "Image.CreateFloatingPositionSize.docx");
```

### Siehe auch

* class [PageSetup](../)
* namensraum [Aspose.Words](../../../aspose.words/)
* Montage [Aspose.Words](../../../)
