---
title: Converter Class
linktitle: Converter
articleTitle: Converter
second_title: Aspose.Words för .NET
description: Konvertera enkelt olika dokumenttyper med Aspose.Words.LowCode.Converter. Förenkla ditt arbetsflöde med bara en rad kod för sömlös integration.
type: docs
weight: 4230
url: /sv/net/aspose.words.lowcode/converter/
---
## Converter class

Representerar en grupp metoder avsedda att konvertera en mängd olika typer av dokument med hjälp av en enda kodrad.

```csharp
public class Converter : Processor
```

## Metoder

| namn | Beskrivning |
| --- | --- |
| static [Create](../../aspose.words.lowcode/converter/create/#create)() | Skapar en ny instans av konverteringsprocessorn. |
| static [Create](../../aspose.words.lowcode/converter/create/#create_1)(*[ConverterContext](../convertercontext/)*) | Skapar en ny instans av konverteringsprocessorn. |
| [Execute](../../aspose.words.lowcode/processor/execute/)() | Utför processoråtgärden. |
| [From](../../aspose.words.lowcode/processor/from/)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Anger indatadokument för bearbetning. |
| [From](../../aspose.words.lowcode/processor/from/)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/)*) | Anger indatadokument för bearbetning. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveFormat](../../aspose.words/saveformat/)*) | Anger listan över utdatadokumentströmmar. |
| [To](../../aspose.words.lowcode/processor/to/)(*List&lt;Stream&gt;, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger listan över utdatadokumentströmmar. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Anger utdataströmmen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger utdataströmmen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Anger utdatafilen för processorn. |
| [To](../../aspose.words.lowcode/processor/to/)(*string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Anger utdatafilen för processorn. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_4)(*string, string*) | Konverterar det givna indatadokumentet till utdatadokumentet med hjälp av angivna indata- och utdatafilnamn och dess filändelser. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_1)(*Stream, Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Konverterar det givna indatadokumentet till ett enda utdatadokument med hjälp av angivna indata- och utdataströmmar. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_2)(*Stream, Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Konverterar det givna indatadokumentet till ett enda utdatadokument med hjälp av angivna indata- och utdataströmmar. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_5)(*string, string, [SaveFormat](../../aspose.words/saveformat/)*) | Konverterar det givna indatadokumentet till utdatadokumentet med hjälp av angivna indata- och utdatafilnamn och det slutliga dokumentformatet. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_6)(*string, string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Konverterar det givna indatadokumentet till utdatadokumentet med hjälp av angivna indata- och utdatafilnamn och sparalternativ. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), Stream, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Konverterar det givna indatadokumentet till ett enda utdatadokument med hjälp av angivna indata- och utdataströmmar. |
| static [Convert](../../aspose.words.lowcode/converter/convert/#convert_3)(*string, [LoadOptions](../../aspose.words.loading/loadoptions/), string, [SaveOptions](../../aspose.words.saving/saveoptions/)*) | Konverterar det givna indatadokumentet till utdatadokumentet med hjälp av angivna indata- och utdatafilnamn och dess laddnings-/spara-alternativ. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_1)(*[Document](../../aspose.words/document/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Konverterar sidorna i det angivna dokumentet till bilder med hjälp av de angivna sparalternativen och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages)(*[Document](../../aspose.words/document/), [SaveFormat](../../aspose.words/saveformat/)*) | Konverterar sidorna i det angivna dokumentet till bilder i det angivna formatet och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_4)(*Stream, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Konverterar sidorna i den angivna indataströmmen till bilder med hjälp av de angivna sparalternativen och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_3)(*Stream, [SaveFormat](../../aspose.words/saveformat/)*) | Konverterar sidorna i den angivna indataströmmen till bilder i det angivna formatet och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_6)(*string, [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Konverterar sidorna i den angivna indatafilen till bilder med hjälp av de angivna sparalternativen och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_5)(*string, [SaveFormat](../../aspose.words/saveformat/)*) | Konverterar sidorna i den angivna indatafilen till bilder i det angivna formatet och returnerar en array av strömmar som innehåller bilderna. |
| static [ConvertToImages](../../aspose.words.lowcode/converter/converttoimages/#converttoimages_2)(*Stream, [LoadOptions](../../aspose.words.loading/loadoptions/), [ImageSaveOptions](../../aspose.words.saving/imagesaveoptions/)*) | Konverterar sidorna i den angivna indataströmmen till bilder med hjälp av de angivna alternativen för laddning och sparning, och returnerar en array av strömmar som innehåller bilderna. |

## Anmärkningar

De angivna in- och utdatafilerna eller strömmarna, tillsammans med önskat sparformat, , används för att konvertera det givna indatadokumentet i det ena formatet till utdatadokumentet i det andra angivna formatet.

Konverteringsfunktionen stöder över 35+ olika filformat.

De[`ConvertToImages`](./converttoimages/)En grupp metoder är utformade för att omvandla dokument till bilder, där varje sida konverteras till en separat bildfil. Dessa metoder konverterar även PDF-dokument direkt till fasta sidformat utan att ladda dem i dokumentmodellen, vilket förbättrar både prestanda och noggrannhet.

Med[`PageSet`](../../aspose.words.saving/imagesaveoptions/pageset/), kan du ange en specifik uppsättning sidor som ska konverteras till bilder.

### Se även

* class [Processor](../processor/)
* namnutrymme [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* hopsättning [Aspose.Words](../../)
