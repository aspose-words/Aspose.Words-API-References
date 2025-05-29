---
title: Watermark.SetImage
linktitle: SetImage
articleTitle: SetImage
second_title: Aspose.Words för .NET
description: Förbättra dina dokument med Watermark SetImage-metoden. Lägg enkelt till fantastiska vattenstämplar för bilder för en professionell touch.
type: docs
weight: 30
url: /sv/net/aspose.words/watermark/setimage/
---
## SetImage(*Image*) {#setimage}

Lägger till bildvattenstämpel i dokumentet.

```csharp
public void SetImage(Image image)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| image | Image | Bild som visas som ett vattenmärke. |

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentNullException | Kasta när bilden är`null` . |

## Exempel

Visar hur man skapar en vattenstämpel från en bild i det lokala filsystemet.

```csharp
Document doc = new Document();

            // Ändra bildens vattenstämpels utseende med ett ImageWatermarkOptions-objekt,
            // skicka sedan den medan du skapar en vattenstämpel från en bildfil.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Vi har olika alternativ för att infoga bilder:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Se även

* class [Watermark](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## SetImage(*Image, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_1}

Lägger till bildvattenstämpel i dokumentet.

```csharp
public void SetImage(Image image, ImageWatermarkOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| image | Image | Bild som visas som ett vattenmärke. |
| options | ImageWatermarkOptions | Definierar ytterligare alternativ för bildens vattenstämpel. |

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentNullException | Kasta när bilden är`null` . |

## Anmärkningar

Om[`ImageWatermarkOptions`](../../imagewatermarkoptions/) är`null`, kommer vattenstämpeln att ställas in med standardalternativen.

## Exempel

Visar hur man skapar en vattenstämpel från en bild i det lokala filsystemet.

```csharp
Document doc = new Document();

            // Ändra bildens vattenstämpels utseende med ett ImageWatermarkOptions-objekt,
            // skicka sedan den medan du skapar en vattenstämpel från en bildfil.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Vi har olika alternativ för att infoga bilder:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Se även

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## SetImage(*string, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_3}

Lägger till bildvattenstämpel i dokumentet.

```csharp
public void SetImage(string imagePath, ImageWatermarkOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| imagePath | String | Sökväg till bildfilen som visas som en vattenstämpel. |
| options | ImageWatermarkOptions | Definierar ytterligare alternativ för bildens vattenstämpel. |

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentNullException | Kasta när sökvägen är`null` . |

## Anmärkningar

Om[`ImageWatermarkOptions`](../../imagewatermarkoptions/) är`null`, kommer vattenstämpeln att ställas in med standardalternativen.

## Exempel

Visar hur man skapar en vattenstämpel från en bild i det lokala filsystemet.

```csharp
Document doc = new Document();

            // Ändra bildens vattenstämpels utseende med ett ImageWatermarkOptions-objekt,
            // skicka sedan den medan du skapar en vattenstämpel från en bildfil.
            ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
            imageWatermarkOptions.Scale = 5;
            imageWatermarkOptions.IsWashout = false;

#if NET461_OR_GREATER || JAVA
            // Vi har olika alternativ för att infoga bilder:
            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"), imageWatermarkOptions);

            doc.Watermark.SetImage(Image.FromFile(ImageDir + "Logo.jpg"));

            doc.Watermark.SetImage(ImageDir + "Logo.jpg", imageWatermarkOptions);
#elif NET5_0_OR_GREATER
            using (SKBitmap image = SKBitmap.Decode(ImageDir + "Logo.jpg"))
            {
                doc.Watermark.SetImage(image, imageWatermarkOptions);
            }
#endif

            doc.Save(ArtifactsDir + "Document.ImageWatermark.docx");
```

### Se även

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)

---

## SetImage(*Stream, [ImageWatermarkOptions](../../imagewatermarkoptions/)*) {#setimage_2}

Lägger till bildvattenstämpel i dokumentet.

```csharp
public void SetImage(Stream imageStream, ImageWatermarkOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| imageStream | Stream | Strömmen som innehåller bilddata som visas som en vattenstämpel. |
| options | ImageWatermarkOptions | Definierar ytterligare alternativ för bildens vattenstämpel. |

### Undantag

| undantag | skick |
| --- | --- |
| ArgumentNullException | Kasta när sökvägen är`null` . |

## Anmärkningar

Om[`ImageWatermarkOptions`](../../imagewatermarkoptions/) är`null`, kommer vattenstämpeln att ställas in med standardalternativen.

## Exempel

Visar hur man skapar en vattenstämpel från en bildström.

```csharp
Document doc = new Document();

// Ändra bildens vattenstämpels utseende med ett ImageWatermarkOptions-objekt,
// skicka sedan den medan du skapar en vattenstämpel från en bildfil.
ImageWatermarkOptions imageWatermarkOptions = new ImageWatermarkOptions();
imageWatermarkOptions.Scale = 5;

using (FileStream imageStream = new FileStream(ImageDir + "Logo.jpg", FileMode.Open, FileAccess.Read))
    doc.Watermark.SetImage(imageStream, imageWatermarkOptions);

doc.Save(ArtifactsDir + "Document.ImageWatermarkStream.docx");
```

### Se även

* class [ImageWatermarkOptions](../../imagewatermarkoptions/)
* class [Watermark](../)
* namnutrymme [Aspose.Words](../../../aspose.words/)
* hopsättning [Aspose.Words](../../../)
