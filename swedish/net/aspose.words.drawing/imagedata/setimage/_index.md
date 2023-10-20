---
title: ImageData.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words för .NET
description: ImageData SetImage metod. Ställer in bilden som formen visar i C#.
type: docs
weight: 200
url: /sv/net/aspose.words.drawing/imagedata/setimage/
---
## SetImage(*Image*) {#setimage}

Ställer in bilden som formen visar.

```csharp
public void SetImage(Image image)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| image | Image | Bildobjektet. |

## Exempel

Visar hur man visar bilder från det lokala filsystemet i ett dokument.

```csharp
Document doc = new Document();

// För att visa en bild i ett dokument måste vi skapa en form
// som kommer att innehålla en bild och sedan lägga till den i dokumentets brödtext.
Shape imgShape;

// Nedan finns två sätt att få en bild från en fil i det lokala filsystemet.
// 1 - Skapa ett bildobjekt från en bildfil:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - Öppna en bildfil från det lokala filsystemet med hjälp av en ström:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Se även

* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

Ställer in bilden som formen visar.

```csharp
public void SetImage(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen som innehåller bilden. |

## Exempel

Visar hur man visar bilder från det lokala filsystemet i ett dokument.

```csharp
Document doc = new Document();

// För att visa en bild i ett dokument måste vi skapa en form
// som kommer att innehålla en bild och sedan lägga till den i dokumentets brödtext.
Shape imgShape;

// Nedan finns två sätt att få en bild från en fil i det lokala filsystemet.
// 1 - Skapa ett bildobjekt från en bildfil:
using (Image srcImage = Image.FromFile(ImageDir + "Logo.jpg"))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(srcImage);
}

// 2 - Öppna en bildfil från det lokala filsystemet med hjälp av en ström:
using (Stream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
{
    imgShape = new Shape(doc, ShapeType.Image);
    doc.FirstSection.Body.FirstParagraph.AppendChild(imgShape);
    imgShape.ImageData.SetImage(stream);
    imgShape.Left = 150.0f;
}

doc.Save(ArtifactsDir + "Drawing.ImportImage.docx");
```

### Se även

* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)

---

## SetImage(*string*) {#setimage_2}

Ställer in bilden som formen visar.

```csharp
public void SetImage(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Bildfilen. Kan vara ett filnamn eller en URL. |

## Exempel

Visar hur man infogar en länkad bild i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFileName = ImageDir + "Windows MetaFile.wmf";

// Nedan finns två sätt att applicera en bild på en form så att den kan visa den.
// 1 - Ställ in formen så att den innehåller bilden.
Shape shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SetImage(imageFileName);

builder.InsertNode(shape);

doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx");

// Varje bild som vi lagrar i form kommer att öka storleken på vårt dokument.
Assert.True(70000 < new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Embedded.docx").Length);

doc.FirstSection.Body.FirstParagraph.RemoveAllChildren();

// 2 - Ställ in formen för att länka till en bildfil i det lokala filsystemet.
shape = new Shape(builder.Document, ShapeType.Image);
shape.WrapType = WrapType.Inline;
shape.ImageData.SourceFullName = imageFileName;

builder.InsertNode(shape);
doc.Save(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx");

// Att länka till bilder sparar utrymme och resulterar i ett mindre dokument.
// Dokumentet kan dock bara visa bilden korrekt medan
// bildfilen finns på den plats som formens "SourceFullName"-egenskap pekar på.
Assert.True(10000 > new FileInfo(ArtifactsDir + "Image.CreateLinkedImage.Linked.docx").Length);
```

### Se även

* class [ImageData](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
