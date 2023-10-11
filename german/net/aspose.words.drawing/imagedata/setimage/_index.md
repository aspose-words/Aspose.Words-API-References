---
title: ImageData.SetImage
second_title: Aspose.Words für .NET-API-Referenz
description: ImageData methode. Legt das Bild fest das die Form anzeigt.
type: docs
weight: 210
url: /de/net/aspose.words.drawing/imagedata/setimage/
---
## SetImage(Image) {#setimage}

Legt das Bild fest, das die Form anzeigt.

```csharp
public void SetImage(Image image)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| image | Image | Das Bildobjekt. |

### Beispiele

Zeigt, wie Bilder aus dem lokalen Dateisystem in einem Dokument angezeigt werden.

```csharp
Document doc = new Document();

// Um ein Bild in einem Dokument anzuzeigen, müssen wir eine Form erstellen
//, das ein Bild enthält, und hängen Sie es dann an den Hauptteil des Dokuments an.
Shape imgShape;

// Nachfolgend finden Sie zwei Möglichkeiten, ein Bild aus einer Datei im lokalen Dateisystem abzurufen.
// 1 – Ein Bildobjekt aus einer Bilddatei erstellen:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 – Öffnen Sie eine Bilddatei aus dem lokalen Dateisystem mithilfe eines Streams:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Siehe auch

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../imagedata/)
* Montage [Aspose.Words](../../../)

---

## SetImage(Stream) {#setimage_1}

Legt das Bild fest, das die Form anzeigt.

```csharp
public void SetImage(Stream stream)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| stream | Stream | Der Stream, der das Bild enthält. |

### Beispiele

Zeigt, wie Bilder aus dem lokalen Dateisystem in einem Dokument angezeigt werden.

```csharp
Document doc = new Document();

// Um ein Bild in einem Dokument anzuzeigen, müssen wir eine Form erstellen
//, das ein Bild enthält, und hängen Sie es dann an den Hauptteil des Dokuments an.
Shape imgShape;

// Nachfolgend finden Sie zwei Möglichkeiten, ein Bild aus einer Datei im lokalen Dateisystem abzurufen.
// 1 – Ein Bildobjekt aus einer Bilddatei erstellen:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 – Öffnen Sie eine Bilddatei aus dem lokalen Dateisystem mithilfe eines Streams:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Siehe auch

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../imagedata/)
* Montage [Aspose.Words](../../../)

---

## SetImage(string) {#setimage_2}

Legt das Bild fest, das die Form anzeigt.

```csharp
public void SetImage(string fileName)
```

| Parameter | Typ | Beschreibung |
| --- | --- | --- |
| fileName | String | Die Bilddatei. Kann ein Dateiname oder eine URL sein. |

### Beispiele

Zeigt, wie ein verknüpftes Bild in ein Dokument eingefügt wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Im Folgenden finden Sie zwei Möglichkeiten, ein Bild auf eine Form anzuwenden, damit diese angezeigt werden kann.
// 1 – Legen Sie die Form so fest, dass sie das Bild enthält.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Jedes Bild, das wir in Form speichern, vergrößert unser Dokument.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 – Legen Sie die Form so fest, dass sie mit einer Bilddatei im lokalen Dateisystem verknüpft wird.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Das Verlinken mit Bildern spart Platz und führt zu einem kleineren Dokument.
// Allerdings kann das Dokument das Bild nur dann korrekt anzeigen, wenn
// Die Bilddatei ist an der Stelle vorhanden, auf die die „SourceFullName“-Eigenschaft der Form verweist.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Siehe auch

* class [ImageData](../)
* namensraum [Aspose.Words.Drawing](../../imagedata/)
* Montage [Aspose.Words](../../../)


