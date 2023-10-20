---
title: Fill.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words för .NET
description: Fill SetImage metod. Ändrar fyllningstypen till en bild i C#.
type: docs
weight: 240
url: /sv/net/aspose.words.drawing/fill/setimage/
---
## SetImage(*string*) {#setimage_2}

Ändrar fyllningstypen till en bild.

```csharp
public void SetImage(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Sökvägen till bildfilen. |

## Exempel

Visar hur du ställer in formfyllningstyp som bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Det finns flera sätt att ställa in bild.
Shape shape = builder.InsertShape(ShapeType.Rectangle, 80, 80);
// 1 - Använda ett lokalt systemfilnamn:
shape.Fill.SetImage(ImageDir + "Logo.jpg");
doc.Save(ArtifactsDir + "Shape.FillImage.FileName.docx");

// 2 - Ladda en fil i en byte-array:
shape.Fill.SetImage(File.ReadAllBytes(ImageDir + "Logo.jpg"));
doc.Save(ArtifactsDir + "Shape.FillImage.ByteArray.docx");

// 3 - Från en ström:
using (FileStream stream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open))
    shape.Fill.SetImage(stream);
doc.Save(ArtifactsDir + "Shape.FillImage.Stream.docx");
```

### Se även

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)

---

## SetImage(*Stream*) {#setimage_1}

Ändrar fyllningstypen till en bild.

```csharp
public void SetImage(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen som innehåller bildbyte. |

### Se även

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)

---

## SetImage(*byte[]*) {#setimage}

Ändrar fyllningstypen till en bild.

```csharp
public void SetImage(byte[] imageBytes)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| imageBytes | Byte[] | Bildbytematrisen. |

### Se även

* class [Fill](../)
* namnutrymme [Aspose.Words.Drawing](../../../aspose.words.drawing/)
* hopsättning [Aspose.Words](../../../)
