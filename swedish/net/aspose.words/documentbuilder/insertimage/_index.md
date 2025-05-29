---
title: DocumentBuilder.InsertImage
linktitle: InsertImage
articleTitle: InsertImage
second_title: Aspose.Words för .NET
description: Förbättra dina dokument enkelt med DocumentBuilders InsertImage-metod, vilket möjliggör sömlös infogning av .NET-bilder i full skala för fantastiska bilder.
type: docs
weight: 400
url: /sv/net/aspose.words/documentbuilder/insertimage/
---
## InsertImage(*Image*) {#insertimage_3}

Infogar en bild från ett .NET-systemImage objekt i dokumentet. Bilden infogas i linje och i 100 % skala.

```csharp
public Shape InsertImage(Image image)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| image | Image | Bilden som ska infogas i dokumentet. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en bild från ett objekt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Nedan följer tre sätt att infoga en bild från en Image-objektinstans.
// 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-form med anpassade dimensioner:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Flytande form med anpassade dimensioner:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertImage(*string*) {#insertimage_9}

Infogar en bild från en fil eller URL i dokumentet. Bilden infogas i rad och i 100 % skala.

```csharp
public Shape InsertImage(string fileName)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Filen med bilden. Kan vara vilken giltig lokal eller fjärr-URI som helst. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Denna överbelastning kommer automatiskt att ladda ner bilden innan den infogas i document om du anger en fjärr-URI.

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar WebP-bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "WebP image.webp");

doc.Save(ArtifactsDir + "Image.InsertWebpImage.docx");
```

Visar hur man infogar en gif-bild i ett dokument.

```csharp
DocumentBuilder builder = new DocumentBuilder();

// Vi kan infoga en gif-bild med hjälp av en sökväg eller en byte-array.
// Det fungerar bara om DocumentBuilder är optimerat för Word version 2010 eller senare.
// Observera att åtkomst till bildens byte orsakar konvertering av GIF till PNG.
Shape gifImage = builder.InsertImage(ImageDir + "Graphics Interchange Format.gif");

gifImage = builder.InsertImage(File.ReadAllBytes(ImageDir + "Graphics Interchange Format.gif"));

builder.Document.Save(ArtifactsDir + "InsertGif.docx");
```

Visar hur man infogar en form med en bild i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan visas två platser där dokumentbyggarens "InsertShape"-metod
// kan skapa källan till bilden som formen ska visa.
// 1 - Skicka ett lokalt filsystemsfilnamn för en bildfil:
builder.Write("Image from local file: ");
builder.InsertImage(ImageDir + "Logo.jpg");
builder.Writeln();

// 2 - Skicka en URL som pekar till en bild.
builder.Write("Image from a URL: ");
builder.InsertImage(ImageUrl);
builder.Writeln();

doc.Save(ArtifactsDir + "Image.FromUrl.docx");
```

Visar hur man infogar en flytande bild i mitten av en sida.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga en flytande bild som visas bakom den överlappande texten och justera den mot sidans mitt.
Shape shape = builder.InsertImage(ImageDir + "Logo.jpg");
shape.WrapType = WrapType.None;
shape.BehindText = true;
shape.RelativeHorizontalPosition = RelativeHorizontalPosition.Page;
shape.RelativeVerticalPosition = RelativeVerticalPosition.Page;
shape.HorizontalAlignment = HorizontalAlignment.Center;
shape.VerticalAlignment = VerticalAlignment.Center;

doc.Save(ArtifactsDir + "Image.CreateFloatingPageCenter.docx");
```

Visar hur man avgör vilken bild som ska infogas.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.InsertImage(ImageDir + "Scalable Vector Graphics.svg");

// Aspose.Words infogar SVG-bild i dokumentet som PNG med tillägget svgBlip
// som innehåller den ursprungliga vektor SVG-bildrepresentationen.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.SvgWithSvgBlip.docx");

// Aspose.Words infogar SVG-bilden i dokumentet som PNG, precis som Microsoft Word gör för det gamla formatet.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Svg.doc");

doc.CompatibilityOptions.OptimizeFor(MsWordVersion.Word2003);

// Aspose.Words infogar SVG-bilden i dokumentet som en EMF-metafil för att behålla bilden i vektorrepresentation.
doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertSvgImage.Emf.docx");
```

Visar hur man infogar en bild från det lokala filsystemet i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer tre sätt att infoga en bild från ett lokalt systemfilnamn.
// 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-form med anpassade dimensioner:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Flytande form med anpassade dimensioner:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertImage(*Stream*) {#insertimage_6}

Infogar en bild från en ström i dokumentet. Bilden infogas i linje och med 100 % skala.

```csharp
public Shape InsertImage(Stream stream)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen som innehåller bilden. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en form med en bild från en ström i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    builder.Write("Image from stream: ");
    builder.InsertImage(stream);
}

doc.Save(ArtifactsDir + "Image.FromStream.docx");
```

Visar hur man infogar en bild från en ström i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Nedan följer tre sätt att infoga en bild från en ström.
    // 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Inline-form med anpassade dimensioner:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Flytande form med anpassade dimensioner:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertImage(*byte[]*) {#insertimage}

Infogar en bild från en byte-array i dokumentet. Bilden infogas i rad och med 100 % skala.

```csharp
public Shape InsertImage(byte[] imageBytes)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| imageBytes | Byte[] | Byte-arrayen som innehåller bilden. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en bild från en byte-array i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Nedan följer tre sätt att infoga en bild från en byte-array.
// 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-form med anpassade dimensioner:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Flytande form med anpassade dimensioner:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertImage(*Image, double, double*) {#insertimage_5}

Infogar en inbäddad bild från ett .NET-systemImage objekt i dokumentet och skalar det till den angivna storleken.

```csharp
public Shape InsertImage(Image image, double width, double height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| image | Image | Bilden som ska infogas i dokumentet. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en bild från ett objekt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Nedan följer tre sätt att infoga en bild från en Image-objektinstans.
// 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-form med anpassade dimensioner:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Flytande form med anpassade dimensioner:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertImage(*string, double, double*) {#insertimage_11}

Infogar en inbäddad bild från en fil eller URL i dokumentet och skalar den till den angivna storleken.

```csharp
public Shape InsertImage(string fileName, double width, double height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Filen som innehåller bilden. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en bild från det lokala filsystemet i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer tre sätt att infoga en bild från ett lokalt systemfilnamn.
// 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-form med anpassade dimensioner:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Flytande form med anpassade dimensioner:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertImage(*Stream, double, double*) {#insertimage_8}

Infogar en inbäddad bild från en ström i dokumentet och skalar den till den angivna storleken.

```csharp
public Shape InsertImage(Stream stream, double width, double height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen som innehåller bilden. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en bild från en ström i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Nedan följer tre sätt att infoga en bild från en ström.
    // 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Inline-form med anpassade dimensioner:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Flytande form med anpassade dimensioner:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertImage(*byte[], double, double*) {#insertimage_2}

Infogar en inbäddad bild från en byte-array i dokumentet och skalar den till den angivna storleken.

```csharp
public Shape InsertImage(byte[] imageBytes, double width, double height)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| imageBytes | Byte[] | Byte-arrayen som innehåller bilden. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en bild från en byte-array i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Nedan följer tre sätt att infoga en bild från en byte-array.
// 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-form med anpassade dimensioner:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Flytande form med anpassade dimensioner:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertImage(*Image, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_4}

Infogar en bild från ett .NET-systemImage objekt på den angivna positionen och storleken.

```csharp
public Shape InsertImage(Image image, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| image | Image | Bilden som ska infogas i dokumentet. |
| horzPos | RelativeHorizontalPosition | Anger varifrån avståndet till bilden mäts. |
| left | Double | Avstånd i punkter från origo till bildens vänstra sida. |
| vertPos | RelativeVerticalPosition | Anger varifrån avståndet till bilden mäts. |
| top | Double | Avstånd i punkter från origo till bildens översida. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | WrapType | Anger hur text ska radbrytas runt bilden. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en bild från ett objekt i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

string imageFile = ImageDir + "Logo.jpg";

// Nedan följer tre sätt att infoga en bild från en Image-objektinstans.
// 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
builder.InsertImage(imageFile);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-form med anpassade dimensioner:
builder.InsertImage(imageFile, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Flytande form med anpassade dimensioner:
builder.InsertImage(imageFile, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromImageObject.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertImage(*string, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_10}

Infogar en bild från en fil eller URL på den angivna positionen och i den angivna storleken.

```csharp
public Shape InsertImage(string fileName, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| fileName | String | Filen som innehåller bilden. |
| horzPos | RelativeHorizontalPosition | Anger varifrån avståndet till bilden mäts. |
| left | Double | Avstånd i punkter från origo till bildens vänstra sida. |
| vertPos | RelativeVerticalPosition | Anger varifrån avståndet till bilden mäts. |
| top | Double | Avstånd i punkter från origo till bildens översida. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | WrapType | Anger hur text ska radbrytas runt bilden. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man lägger in en bild.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Det finns två sätt att använda en dokumentbyggare för att skapa en bild och sedan infoga den som en flytande form.
// 1 - Från en fil i det lokala filsystemet:
builder.InsertImage(ImageDir + "Transparent background logo.png", RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 0, 200, 200, WrapType.Square);

// 2 - Från en URL:
builder.InsertImage(ImageUrl, RelativeHorizontalPosition.Margin, 100,
    RelativeVerticalPosition.Margin, 250, 200, 200, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFloatingImage.docx");
```

Visar hur man infogar en bild från det lokala filsystemet i ett dokument samtidigt som dess dimensioner bevaras.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metoden InsertImage skapar en flytande form med den skickade bilden i dess bilddata.
// Vi kan ange formens dimensioner och skicka dem till den här metoden.
Shape imageShape = builder.InsertImage(ImageDir + "Logo.jpg", RelativeHorizontalPosition.Margin, 0,
    RelativeVerticalPosition.Margin, 0, -1, -1, WrapType.Square);

// Att skicka negativa värden som avsedda dimensioner kommer automatiskt att definiera
// formens dimensioner baserat på dimensionerna på dess bild.
Assert.AreEqual(300.0d, imageShape.Width);
Assert.AreEqual(300.0d, imageShape.Height);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertImageOriginalSize.docx");
```

Visar hur man infogar en bild från det lokala filsystemet i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Nedan följer tre sätt att infoga en bild från ett lokalt systemfilnamn.
// 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
builder.InsertImage(ImageDir + "Logo.jpg");

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-form med anpassade dimensioner:
builder.InsertImage(ImageDir + "Transparent background logo.png", ConvertUtil.PixelToPoint(250),
    ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Flytande form med anpassade dimensioner:
builder.InsertImage(ImageDir + "Windows MetaFile.wmf", RelativeHorizontalPosition.Margin, 100, 
    RelativeVerticalPosition.Margin, 100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromFilename.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertImage(*Stream, [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_7}

Infogar en bild från en ström på den angivna positionen och i den angivna storleken.

```csharp
public Shape InsertImage(Stream stream, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| stream | Stream | Strömmen som innehåller bilden. |
| horzPos | RelativeHorizontalPosition | Anger varifrån avståndet till bilden mäts. |
| left | Double | Avstånd i punkter från origo till bildens vänstra sida. |
| vertPos | RelativeVerticalPosition | Anger varifrån avståndet till bilden mäts. |
| top | Double | Avstånd i punkter från origo till bildens översida. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | WrapType | Anger hur text ska radbrytas runt bilden. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en bild från en ström i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

using (Stream stream = File.OpenRead(ImageDir + "Logo.jpg"))
{
    // Nedan följer tre sätt att infoga en bild från en ström.
    // 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
    builder.InsertImage(stream);

    builder.InsertBreak(BreakType.PageBreak);

    // 2 - Inline-form med anpassade dimensioner:
    builder.InsertImage(stream, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

    builder.InsertBreak(BreakType.PageBreak);

    // 3 - Flytande form med anpassade dimensioner:
    builder.InsertImage(stream, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
        100, 200, 100, WrapType.Square);
}

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromStream.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## InsertImage(*byte[], [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/), double, [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/), double, double, double, [WrapType](../../../aspose.words.drawing/wraptype/)*) {#insertimage_1}

Infogar en bild från en byte-array på den angivna positionen och storleken.

```csharp
public Shape InsertImage(byte[] imageBytes, RelativeHorizontalPosition horzPos, double left, 
    RelativeVerticalPosition vertPos, double top, double width, double height, WrapType wrapType)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| imageBytes | Byte[] | Byte-arrayen som innehåller bilden. |
| horzPos | RelativeHorizontalPosition | Anger varifrån avståndet till bilden mäts. |
| left | Double | Avstånd i punkter från origo till bildens vänstra sida. |
| vertPos | RelativeVerticalPosition | Anger varifrån avståndet till bilden mäts. |
| top | Double | Avstånd i punkter från origo till bildens översida. |
| width | Double | Bildens bredd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| height | Double | Bildens höjd i punkter. Kan vara ett negativt eller nollvärde för att begära 100 % skala. |
| wrapType | WrapType | Anger hur text ska radbrytas runt bilden. |

### Returvärde

Bildnoden som just infogades.

## Anmärkningar

Du kan ändra bildstorlek, plats, positioneringsmetod och andra inställningar med hjälp av [`Shape`](../../../aspose.words.drawing/shape/) objekt som returneras av den här metoden.

## Exempel

Visar hur man infogar en bild från en byte-array i ett dokument.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

byte[] imageByteArray = TestUtil.ImageToByteArray(ImageDir + "Logo.jpg");

// Nedan följer tre sätt att infoga en bild från en byte-array.
// 1 - Inline-form med en standardstorlek baserad på bildens ursprungliga mått:
builder.InsertImage(imageByteArray);

builder.InsertBreak(BreakType.PageBreak);

// 2 - Inline-form med anpassade dimensioner:
builder.InsertImage(imageByteArray, ConvertUtil.PixelToPoint(250), ConvertUtil.PixelToPoint(144));

builder.InsertBreak(BreakType.PageBreak);

// 3 - Flytande form med anpassade dimensioner:
builder.InsertImage(imageByteArray, RelativeHorizontalPosition.Margin, 100, RelativeVerticalPosition.Margin,
100, 200, 100, WrapType.Square);

doc.Save(ArtifactsDir + "DocumentBuilderImages.InsertImageFromByteArray.docx");
```

### Se även

* class [Shape](../../../aspose.words.drawing/shape/)
* enum [RelativeHorizontalPosition](../../../aspose.words.drawing/relativehorizontalposition/)
* enum [RelativeVerticalPosition](../../../aspose.words.drawing/relativeverticalposition/)
* enum [WrapType](../../../aspose.words.drawing/wraptype/)
* class [DocumentBuilder](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
