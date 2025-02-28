---
title: Fill.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words for .NET
description: Enhance your design with the SetImage method. Easily switch to a single image fill type for stunning visuals and seamless integration.
type: docs
weight: 250
url: /net/aspose.words.drawing/fill/setimage/
---
## SetImage(*string*) {#setimage_2}

Changes the fill type to single image.

```csharp
public void SetImage(string fileName)
```

| Parameter | Type | Description |
| --- | --- | --- |
| fileName | String | The path to the image file. |

## Examples

Shows how to set shape fill type as image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// There are several ways of setting image.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 -  Using a local system filename:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 -  Load a file into a byte array:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 -  From a stream:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### See Also

* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

Changes the fill type to single image.

```csharp
public void SetImage(Stream stream)
```

| Parameter | Type | Description |
| --- | --- | --- |
| stream | Stream | The stream that contains the image bytes. |

## Examples

Shows how to set shape fill type as image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// There are several ways of setting image.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 -  Using a local system filename:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 -  Load a file into a byte array:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 -  From a stream:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### See Also

* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)

---

## SetImage(*byte[]*) {#setimage}

Changes the fill type to single image.

```csharp
public void SetImage(byte[] imageBytes)
```

| Parameter | Type | Description |
| --- | --- | --- |
| imageBytes | Byte[] | The image bytes array. |

## Examples

Shows how to set shape fill type as image.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// There are several ways of setting image.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 -  Using a local system filename:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 -  Load a file into a byte array:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 -  From a stream:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### See Also

* class [Fill](../)
* namespace [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* assembly [Aspose.Words](../../../)
