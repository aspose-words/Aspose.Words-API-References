---
title: Converter.Convert
linktitle: Convert
articleTitle: Convert
second_title: Aspose.Words för .NET
description: Konvertera dina dokument enkelt med vår konverterares konverteringsmetod. Omvandla indatafiler till önskade format med lätthet och precision.
type: docs
weight: 20
url: /sv/net/aspose.words.lowcode/converter/convert/
---
## Convert(*string, string*) {#convert_4}

Konverterar det givna indatadokumentet till utdatadokumentet med hjälp av angivna indata- och utdatafilnamn och dess filändelser.

```csharp
public static void Convert(string inputFile, string outputFile)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFile | String | Namnet på inmatningsfilen. |
| outputFile | String | Namnet på utdatafilen. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man konverterar dokument med en enda kodrad.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Se även

* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_5}

Konverterar det givna indatadokumentet till utdatadokumentet med hjälp av angivna indata- och utdatafilnamn och det slutliga dokumentformatet.

```csharp
public static void Convert(string inputFile, string outputFile, SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFile | String | Namnet på inmatningsfilen. |
| outputFile | String | Namnet på utdatafilen. |
| saveFormat | SaveFormat | Sparformatet. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man konverterar dokument med en enda kodrad.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Convert(*string, string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_6}

Konverterar det givna indatadokumentet till utdatadokumentet med hjälp av angivna indata- och utdatafilnamn och sparalternativ.

```csharp
public static void Convert(string inputFile, string outputFile, SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFile | String | Namnet på inmatningsfilen. |
| outputFile | String | Namnet på utdatafilen. |
| saveOptions | SaveOptions | Sparalternativen. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man konverterar dokument med en enda kodrad.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Convert(*string, [LoadOptions](../../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_3}

Konverterar det givna indatadokumentet till utdatadokumentet med hjälp av angivna indata- och utdatafilnamn och dess laddnings-/spara-alternativ.

```csharp
public static void Convert(string inputFile, LoadOptions loadOptions, string outputFile, 
    SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFile | String | Namnet på inmatningsfilen. |
| loadOptions | LoadOptions | Alternativ för inläsning av inmatningsdokument. |
| outputFile | String | Namnet på utdatafilen. |
| saveOptions | SaveOptions | Sparalternativen. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas varje sida av utdatafilen som en separat fil. Det angivna utdatafilnamnet används för att generera filnamn för varje del enligt regeln: outputFile_partIndex.extension.

Om utdataformatet är TIFF sparas utdata som en enda TIFF-fil med flera bildrutor.

## Exempel

Visar hur man konverterar dokument med en enda kodrad.

```csharp
string doc = MyDir + "Document.docx";

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.pdf");

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveFormat.rtf", SaveFormat.Rtf);

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
Converter.Convert(doc, loadOptions, ArtifactsDir + "LowCode.Convert.LoadOptions.docx", saveOptions);

Converter.Convert(doc, ArtifactsDir + "LowCode.Convert.SaveOptions.docx", saveOptions);
```

### Se även

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#convert_1}

Konverterar det givna indatadokumentet till ett enda utdatadokument med hjälp av angivna indata- och utdataströmmar.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| outputStream | Stream | Utgångsströmmen. |
| saveFormat | SaveFormat | Sparformatet. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

## Exempel

Visar hur man konverterar dokument med en enda kodrad (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Convert(*Stream, Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert_2}

Konverterar det givna indatadokumentet till ett enda utdatadokument med hjälp av angivna indata- och utdataströmmar.

```csharp
public static void Convert(Stream inputStream, Stream outputStream, SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmarna. |
| outputStream | Stream | Utgångsströmmen. |
| saveOptions | SaveOptions | Sparalternativen. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

## Exempel

Visar hur man konverterar dokument med en enda kodrad (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Se även

* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## Convert(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../../aspose.words.saving/saveoptions/)*) {#convert}

Konverterar det givna indatadokumentet till ett enda utdatadokument med hjälp av angivna indata- och utdataströmmar.

```csharp
public static void Convert(Stream inputStream, LoadOptions loadOptions, Stream outputStream, 
    SaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmarna. |
| loadOptions | LoadOptions | Alternativ för inläsning av inmatningsdokument. |
| outputStream | Stream | Utgångsströmmen. |
| saveOptions | SaveOptions | Sparalternativen. |

## Anmärkningar

Om utdataformatet är en bild (BMP, EMF, EPS, GIF, JPEG, PNG eller WebP) sparas endast den första sidan av utdata i den angivna strömmen.

Om utdataformatet är TIFF sparas utdata som en enda TIFF med flera bildrutor till den angivna strömmen.

## Exempel

Visar hur man konverterar dokument med en enda kodrad (Stream).

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.1.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, SaveFormat.Docx);

    OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = true };
    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.2.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, loadOptions, streamOut, saveOptions);

    using (FileStream streamOut = new FileStream(ArtifactsDir + "LowCode.ConvertStream.3.docx", FileMode.Create, FileAccess.ReadWrite))
        Converter.Convert(streamIn, streamOut, saveOptions);
}
```

### Se även

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [SaveOptions](../../../aspose.words.saving/saveoptions/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
