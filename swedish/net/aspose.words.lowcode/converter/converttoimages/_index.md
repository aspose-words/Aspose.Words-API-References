---
title: Converter.ConvertToImages
linktitle: ConvertToImages
articleTitle: ConvertToImages
second_title: Aspose.Words för .NET
description: Förvandla dina dokument enkelt med ConvertToImages. Konvertera sidor till högkvalitativa bildfiler snabbt och enkelt för förbättrad delning och lagring.
type: docs
weight: 30
url: /sv/net/aspose.words.lowcode/converter/converttoimages/
---
## ConvertToImages(*string, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_5}

Konverterar sidorna i den angivna indatafilen till bilder i det angivna formatet och returnerar en array av strömmar som innehåller bilderna.

```csharp
public static Stream[] ConvertToImages(string inputFile, SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFile | String | Namnet på inmatningsfilen. |
| saveFormat | SaveFormat | Sparformat. Endast bildformat är tillåtna. |

### Returvärde

Returnerar en array av bildströmmar. Strömmarna ska kasseras av slutanvändaren.

## Exempel

Visar hur man konverterar dokument till bildström.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ConvertToImages(*string, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_6}

Konverterar sidorna i den angivna indatafilen till bilder med hjälp av de angivna sparalternativen och returnerar en array av strömmar som innehåller bilderna.

```csharp
public static Stream[] ConvertToImages(string inputFile, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputFile | String | Namnet på inmatningsfilen. |
| saveOptions | ImageSaveOptions | Alternativ för att spara bilder. |

### Returvärde

Returnerar en array av bildströmmar. Strömmarna ska kasseras av slutanvändaren.

## Exempel

Visar hur man konverterar dokument till bildström.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages_3}

Konverterar sidorna i den angivna indataströmmen till bilder i det angivna formatet och returnerar en array av strömmar som innehåller bilderna.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| saveFormat | SaveFormat | Sparformat. Endast bildformat är tillåtna. |

### Returvärde

Returnerar en array av bildströmmar. Strömmarna ska kasseras av slutanvändaren.

## Exempel

Visar hur man konverterar dokument till bilder från ström.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Se även

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_4}

Konverterar sidorna i den angivna indataströmmen till bilder med hjälp av de angivna sparalternativen och returnerar en array av strömmar som innehåller bilderna.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| saveOptions | ImageSaveOptions | Alternativ för att spara bilder. |

### Returvärde

Returnerar en array av bildströmmar. Strömmarna ska kasseras av slutanvändaren.

## Exempel

Visar hur man konverterar dokument till bilder från ström.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Se även

* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ConvertToImages(*Stream, [LoadOptions](../../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_2}

Konverterar sidorna i den angivna indataströmmen till bilder med hjälp av de angivna alternativen för laddning och sparning, och returnerar en array av strömmar som innehåller bilderna.

```csharp
public static Stream[] ConvertToImages(Stream inputStream, LoadOptions loadOptions, 
    ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| inputStream | Stream | Ingångsströmmen. |
| loadOptions | LoadOptions | Alternativ för inläsning av inmatningsdokument. |
| saveOptions | ImageSaveOptions | Alternativ för att spara bilder. |

### Returvärde

Returnerar en array av bildströmmar. Strömmarna ska kasseras av slutanvändaren.

## Exempel

Visar hur man konverterar dokument till bilder från ström.

```csharp
using (FileStream streamIn = new FileStream(MyDir + "Big document.docx", FileMode.Open, FileAccess.Read))
{
    Stream[] streams = Converter.ConvertToImages(streamIn, SaveFormat.Jpeg);

    ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
    imageSaveOptions.PageSet = new PageSet(1);
    streams = Converter.ConvertToImages(streamIn, imageSaveOptions);

    LoadOptions loadOptions = new LoadOptions() { IgnoreOleData = false };
    Converter.ConvertToImages(streamIn, loadOptions, imageSaveOptions);
}
```

### Se även

* class [LoadOptions](../../../aspose.words.loading/loadoptions/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [SaveFormat](../../../aspose.words/saveformat/)*) {#converttoimages}

Konverterar sidorna i det angivna dokumentet till bilder i det angivna formatet och returnerar en array av strömmar som innehåller bilderna.

```csharp
public static Stream[] ConvertToImages(Document doc, SaveFormat saveFormat)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | Document | Inmatningsdokumentet. |
| saveFormat | SaveFormat | Sparformat. Endast bildformat är tillåtna. |

### Returvärde

Returnerar en array av bildströmmar. Strömmarna ska kasseras av slutanvändaren.

## Exempel

Visar hur man konverterar dokument till bildström.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Se även

* class [Document](../../../aspose.words/document/)
* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)

---

## ConvertToImages(*[Document](../../../aspose.words/document/), [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)*) {#converttoimages_1}

Konverterar sidorna i det angivna dokumentet till bilder med hjälp av de angivna sparalternativen och returnerar en array av strömmar som innehåller bilderna.

```csharp
public static Stream[] ConvertToImages(Document doc, ImageSaveOptions saveOptions)
```

| Parameter | Typ | Beskrivning |
| --- | --- | --- |
| doc | Document | Inmatningsdokumentet. |
| saveOptions | ImageSaveOptions | Alternativ för att spara bilder. |

### Returvärde

Returnerar en array av bildströmmar. Strömmarna ska kasseras av slutanvändaren.

## Exempel

Visar hur man konverterar dokument till bildström.

```csharp
string doc = MyDir + "Big document.docx";

Stream[] streams = Converter.ConvertToImages(doc, SaveFormat.Png);

ImageSaveOptions imageSaveOptions = new ImageSaveOptions(SaveFormat.Png);
imageSaveOptions.PageSet = new PageSet(1);
streams = Converter.ConvertToImages(doc, imageSaveOptions);

streams = Converter.ConvertToImages(new Document(doc), SaveFormat.Png);

streams = Converter.ConvertToImages(new Document(doc), imageSaveOptions);
```

### Se även

* class [Document](../../../aspose.words/document/)
* class [ImageSaveOptions](../../../aspose.words.saving/imagesaveoptions/)
* class [Converter](../)
* namnutrymme [Aspose.Words.LowCode](../../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../../)
