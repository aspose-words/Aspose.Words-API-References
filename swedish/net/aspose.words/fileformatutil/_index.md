---
title: Class FileFormatUtil
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.FileFormatUtil klass. Tillhandahåller verktygsmetoder för att arbeta med filformat som att upptäcka filformat eller konvertera filtillägg till/från filformat enums.
type: docs
weight: 2820
url: /sv/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Tillhandahåller verktygsmetoder för att arbeta med filformat, som att upptäcka filformat eller konvertera filtillägg till/från filformat enums.

För att lära dig mer, besök[Upptäck filformat och kontrollera formatkompatibilitet](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) dokumentationsartikel.

```csharp
public static class FileFormatUtil
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(string) | Konverterar IANA-innehållstyp till ett laddningsformat uppräknat värde. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(string) | Konverterar IANA-innehållstyp till ett sparat format uppräknat värde. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(Stream) | Upptäcker och returnerar information om formatet för ett dokument som lagras i en ström. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(string) | Upptäcker och returnerar information om formatet för ett dokument som lagras i en diskfil. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(string) | Konverterar ett filnamnstillägg till en[`SaveFormat`](../saveformat/) värde. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(ImageType) | Konverterar ett uppräknat värde av bildtyp Aspose.Words till ett filtillägg. Det returnerade tillägget är en sträng med små bokstäver med en inledande punkt. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(LoadFormat) | Konverterar ett laddningsformat uppräknat värde till ett filtillägg. Det returnerade tillägget är en sträng med små bokstäver med en inledande punkt. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(LoadFormat) | Konverterar en[`LoadFormat`](../loadformat/) värde till a[`SaveFormat`](../saveformat/) värde om möjligt. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(SaveFormat) | Konverterar ett sparat format uppräknat värde till ett filtillägg. Det returnerade tillägget är en sträng med små bokstäver med en inledande punkt. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(SaveFormat) | Konverterar en[`SaveFormat`](../saveformat/) värde till a[`LoadFormat`](../loadformat/) värde om möjligt. |

### Exempel

Visar hur man upptäcker kodning i en html-fil.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Encoding-egenskapen används endast när vi skapar ett FileFormatInfo-objekt för ett HTML-dokument.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)


