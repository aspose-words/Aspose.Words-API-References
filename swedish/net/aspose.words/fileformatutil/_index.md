---
title: FileFormatUtil Class
linktitle: FileFormatUtil
articleTitle: FileFormatUtil
second_title: Aspose.Words för .NET
description: Hantera filformat enkelt med Aspose.Words.FileFormatUtil. Identifiera format och konvertera filändelser sömlöst för ökad produktivitet.
type: docs
weight: 3230
url: /sv/net/aspose.words/fileformatutil/
---
## FileFormatUtil class

Tillhandahåller verktygsmetoder för att arbeta med filformat, till exempel att identifiera filformat eller konvertera filändelser till/från filformatuppräkningar.

För att lära dig mer, besök[Identifiera filformat och kontrollera formatkompatibilitet](https://docs.aspose.com/words/net/detect-file-format-and-check-format-compatibility/) dokumentationsartikel.

```csharp
public static class FileFormatUtil
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [ContentTypeToLoadFormat](../../aspose.words/fileformatutil/contenttypetoloadformat/)(*string*) | Konverterar IANA-innehållstypen till ett uppräknat värde i laddningsformat. |
| static [ContentTypeToSaveFormat](../../aspose.words/fileformatutil/contenttypetosaveformat/)(*string*) | Konverterar IANA-innehållstypen till ett uppräknat värde i sparformat. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat)(*Stream*) | Upptäcker och returnerar information om formatet för ett dokument som lagras i en ström. |
| static [DetectFileFormat](../../aspose.words/fileformatutil/detectfileformat/#detectfileformat_1)(*string*) | Upptäcker och returnerar information om formatet för ett dokument som lagras i en diskfil. |
| static [ExtensionToSaveFormat](../../aspose.words/fileformatutil/extensiontosaveformat/)(*string*) | Konverterar ett filnamnstillägg till en[`SaveFormat`](../saveformat/) värde. |
| static [ImageTypeToExtension](../../aspose.words/fileformatutil/imagetypetoextension/)(*[ImageType](../../aspose.words.drawing/imagetype/)*) | Konverterar ett uppräknat värde av bildtypen Aspose.Words till en filändelse. Den returnerade filändelsen är en liten sträng med en inledande punkt. |
| static [LoadFormatToExtension](../../aspose.words/fileformatutil/loadformattoextension/)(*[LoadFormat](../loadformat/)*) | Konverterar ett uppräknat värde i laddningsformat till en filändelse. Den returnerade filändelsen är en liten sträng med en inledande punkt. |
| static [LoadFormatToSaveFormat](../../aspose.words/fileformatutil/loadformattosaveformat/)(*[LoadFormat](../loadformat/)*) | Konverterar en[`LoadFormat`](../loadformat/) värde till en[`SaveFormat`](../saveformat/) värde om möjligt. |
| static [SaveFormatToExtension](../../aspose.words/fileformatutil/saveformattoextension/)(*[SaveFormat](../saveformat/)*) | Konverterar ett uppräknat värde i sparformat till en filändelse. Den returnerade filändelsen är en liten sträng med en inledande punkt. |
| static [SaveFormatToLoadFormat](../../aspose.words/fileformatutil/saveformattoloadformat/)(*[SaveFormat](../saveformat/)*) | Konverterar en[`SaveFormat`](../saveformat/) värde till en[`LoadFormat`](../loadformat/) värde om möjligt. |

## Exempel

Visar hur man identifierar kodning i en html-fil.

```csharp
FileFormatInfo info = FileFormatUtil.DetectFileFormat(MyDir + "Document.html");

Assert.AreEqual(LoadFormat.Html, info.LoadFormat);

// Egenskapen Encoding används endast när vi skapar ett FileFormatInfo-objekt för ett HTML-dokument.
Assert.AreEqual("Western European (Windows)", info.Encoding.EncodingName);
Assert.AreEqual(1252, info.Encoding.CodePage);
```

### Se även

* namnutrymme [Aspose.Words](../../aspose.words/)
* hopsättning [Aspose.Words](../../)
