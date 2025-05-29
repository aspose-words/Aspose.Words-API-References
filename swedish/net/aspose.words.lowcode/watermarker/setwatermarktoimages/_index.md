---
title: Watermarker.SetWatermarkToImages
linktitle: SetWatermarkToImages
articleTitle: SetWatermarkToImages
second_title: Aspose.Words för .NET
description: Förbättra dina bilder med vår vattenstämpelmetod och lägg till anpassningsbara textvattenstämplar för en professionell touch och sömlös utskrift.
type: docs
weight: 40
url: /sv/net/aspose.words.lowcode/watermarker/setwatermarktoimages/
---
## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_3}

Lägger till en textvattenstämpel i dokumentet med alternativ. Återger utdata till bilder.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| saveOptions | ImageSaveOptions | Sparalternativen. |
| watermarkText | String | Text som visas som en vattenstämpel. |
| options | TextWatermarkOptions | Definierar ytterligare alternativ för textvattenmärket. |

## Exempel

Visar hur man infogar vattenstämpeltext i dokumentet och sparar resultatet som bilder.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Stream[] images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText);

TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
images = Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#setwatermarktoimages_1}

Lägger till en textvattenstämpel i dokumentet med alternativ. Återger utdata till bilder.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Indatafilströmmen. |
| saveOptions | ImageSaveOptions | Sparalternativen. |
| watermarkText | String | Text som visas som en vattenstämpel. |
| options | TextWatermarkOptions | Definierar ytterligare alternativ för textvattenmärket. |

## Exempel

Visar hur man infogar vattenstämpeltext i dokumentet från strömmen och sparar resultatet som bilder.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText);

    TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
    watermarkOptions.Color = Color.Red;
    images = Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), watermarkText, watermarkOptions);
}
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## SetWatermarkToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), byte[], [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages_2}

Lägger till en bildvattenstämpel i dokumentet med alternativ. Återger utdata till bilder.

```csharp
public static Stream[] SetWatermarkToImages(string inputFileName, ImageSaveOptions saveOptions, 
    byte[] watermarkImageBytes, ImageWatermarkOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| saveOptions | ImageSaveOptions | Sparalternativen. |
| watermarkImageBytes | Byte[] | Bildbyte som visas som ett vattenmärke. |
| options | ImageWatermarkOptions | Definierar ytterligare alternativ för bildens vattenstämpel. |

## Exempel

Visar hur man infogar en vattenstämpelbild i dokumentet och sparar resultatet som bilder.

```csharp
string doc = MyDir + "Document.docx";
string watermarkImage = ImageDir + "Logo.jpg";

Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage));

ImageWatermarkOptions options = new ImageWatermarkOptions();
options.Scale = 50;
Watermarker.SetWatermarkToImages(doc, new ImageSaveOptions(SaveFormat.Png), File.ReadAllBytes(watermarkImage), options);
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## SetWatermarkToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/), Stream, [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)*) {#setwatermarktoimages}

Lägger till en bildvattenstämpel i dokumentet med alternativ. Återger utdata till bilder.

```csharp
public static Stream[] SetWatermarkToImages(Stream inputStream, ImageSaveOptions saveOptions, 
    Stream watermarkImageStream, ImageWatermarkOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| saveOptions | ImageSaveOptions | Sparalternativen. |
| watermarkImageStream | Stream | Bildström som visas som ett vattenmärke. |
| options | ImageWatermarkOptions | Definierar ytterligare alternativ för bildens vattenstämpel. |

## Exempel

Visar hur man infogar en vattenstämpelbild i dokumentet från en ström och sparar resultatet som bilder.

```csharp
string watermarkImage = ImageDir + "Logo.jpg";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream imageStream = new FileStream(watermarkImage, FileMode.Open, FileAccess.Read))
    {
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream);
        Watermarker.SetWatermarkToImages(streamIn, new ImageSaveOptions(SaveFormat.Png), imageStream, new ImageWatermarkOptions() { Scale = 50 });
    }
}
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [ImageWatermarkOptions](../../../aspose.words/imagewatermarkoptions/)
* class [Watermarker](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
