---
title: Watermarker.SetText
linktitle: SetText
articleTitle: SetText
second_title: Aspose.Words för .NET
description: Förbättra dina dokument med vår metod Watermarker SetText. Lägg enkelt till anpassningsbara textvattenmärken för förbättrad varumärkesprofilering och professionalism.
type: docs
weight: 30
url: /sv/net/aspose.words.lowcode/watermarker/settext/
---
## SetText(*string, string, string*) {#settext_4}

Lägger till en vattenstämpel i dokumentet.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| watermarkText | String | Text som visas som en vattenstämpel. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man infogar vattenstämpeltext i dokumentet.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Se även

* class [Watermarker](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## SetText(*string, string, string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_5}

Lägger till en textvattenstämpel i dokumentet med alternativ.

```csharp
public static void SetText(string inputFileName, string outputFileName, string watermarkText, 
    TextWatermarkOptions options)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| watermarkText | String | Text som visas som en vattenstämpel. |
| options | TextWatermarkOptions | Definierar ytterligare alternativ för textvattenmärket. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man infogar vattenstämpeltext i dokumentet.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Se även

* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_2}

Lägger till en textvattenstämpel i dokumentet med alternativ och angivet sparformat.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveFormat | SaveFormat | Sparformatet. |
| watermarkText | String | Text som visas som en vattenstämpel. |
| options | TextWatermarkOptions | Definierar ytterligare alternativ för textvattenmärket. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man infogar vattenstämpeltext i dokumentet.

```csharp
string doc = MyDir + "Big document.docx";
string watermarkText = "This is a watermark";

Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.1.docx", watermarkText);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.2.docx", SaveFormat.Docx, watermarkText);
TextWatermarkOptions watermarkOptions = new TextWatermarkOptions();
watermarkOptions.Color = Color.Red;
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.3.docx", watermarkText, watermarkOptions);
Watermarker.SetText(doc, ArtifactsDir + "LowCode.WatermarkText.4.docx", SaveFormat.Docx, watermarkText, watermarkOptions);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## SetText(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_3}

Lägger till en textvattenstämpel i dokumentet med alternativ och angivet sparformat.

```csharp
public static void SetText(string inputFileName, string outputFileName, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFileName | String | Namnet på inmatningsfilen. |
| outputFileName | String | Namnet på utdatafilen. |
| saveOptions | SaveOptions | Sparalternativen. |
| watermarkText | String | Text som visas som en vattenstämpel. |
| options | TextWatermarkOptions | Definierar ytterligare alternativ för textvattenmärket. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext}

Lägger till en textvattenstämpel i dokumentet från strömmar med alternativ.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveFormat saveFormat, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| outputStream | Stream | Utgångsströmmen. |
| saveFormat | SaveFormat | Sparformatet. |
| watermarkText | String | Text som visas som en vattenstämpel. |
| options | TextWatermarkOptions | Definierar ytterligare alternativ för textvattenmärket. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

## Exempel

Visar hur man infogar vattenstämpeltext i dokumentet från strömmen.

```csharp
string watermarkText = "This is a watermark";

using (FileStream streamIn = new FileStream(MyDir + "Document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.WatermarkTextStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
    {
        TextWatermarkOptions options = new TextWatermarkOptions();
        options.Color = Color.Red;
        Watermarker.SetText(streamIn, streamOut, SaveFormat.Docx, watermarkText, options);
    }
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## SetText(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/), string, [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)*) {#settext_1}

Lägger till en textvattenstämpel i dokumentet från strömmar med alternativ.

```csharp
public static void SetText(Stream inputStream, Stream outputStream, SaveOptions saveOptions, 
    string watermarkText, TextWatermarkOptions options = null)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| outputStream | Stream | Utgångsströmmen. |
| saveOptions | SaveOptions | Sparalternativen. |
| watermarkText | String | Text som visas som en vattenstämpel. |
| options | TextWatermarkOptions | Definierar ytterligare alternativ för textvattenmärket. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [TextWatermarkOptions](../../../aspose.words/textwatermarkoptions/)
* class [Watermarker](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
