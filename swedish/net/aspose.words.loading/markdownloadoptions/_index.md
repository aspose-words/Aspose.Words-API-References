---
title: MarkdownLoadOptions Class
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.MarkdownLoadOptions för att förbättra din Markdown-dokumentinläsningsupplevelse. Anpassa alternativ för sömlös integration i dina projekt.
type: docs
weight: 4120
url: /sv/net/aspose.words.loading/markdownloadoptions/
---
## MarkdownLoadOptions class

Gör det möjligt att ange ytterligare alternativ vid laddningMarkdown dokument till ett[`Document`](../../aspose.words/document/) objekt.

```csharp
public class MarkdownLoadOptions : LoadOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [MarkdownLoadOptions](markdownloadoptions/)() | Initierar en ny instans av`MarkdownLoadOptions` klass. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Hämtar eller ställer in strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er vid behov. Kan vara`null` eller tom sträng. Standard är`null` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Hämtar eller anger om metafil ska konverteras(Wmf ellerEmf ) bilder tillPngbildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Hämtar eller anger om former ska konverteras med EquationXML till Office Math-objekt. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Hämtar eller anger kodningen som ska användas för att läsa in ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad i dokumentet. Kan vara`null` Standard är`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Gör det möjligt att ange dokumentets teckensnittsinställningar. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Anger om OLE-data ska ignoreras. |
| [ImportUnderlineFormatting](../../aspose.words.loading/markdownloadoptions/importunderlineformatting/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger att en sekvens av två plustecken "++" ska kännas igen som understruken textformatering. Standardvärdet är`falsk` . |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Hämtar språkinställningar som kommer att användas när dokumentet laddas. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Anger formatet för det dokument som ska läsas in. Standard ärAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Gör det möjligt att ange att dokumentinläsningsprocessen ska matcha en specifik MS Word-version. Standardvärdet ärWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Hämtar eller ställer in lösenordet för att öppna ett krypterat dokument. Kan vara`null` eller tom sträng. Standard är`null` . |
| [PreserveEmptyLines](../../aspose.words.loading/markdownloadoptions/preserveemptylines/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger om tomma rader ska behållas vid laddning av enMarkdown dokument. Standardvärdet är`falsk` . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Hämtar eller anger om fältet INCLUDEPICTURE ska bevaras vid läsning av Microsoft Word-format. Standardvärdet är`falsk` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Anropas under laddning av ett dokument och accepterar data om laddningsförloppet. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Gör det möjligt att styra hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Tillåter användning av temporära filer vid läsning av dokument. Som standard är den här egenskapen`null` och inga temporära filer används. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Anger om fälten ska uppdateras med`smutsig` attribut. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Hämtar eller anger om LCID-värde från Windows-registret ska användas för att bestämma standardmarginaler för sidinställningar. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Anropas under en inläsningsoperation, när ett problem upptäcks som kan leda till förlust av data- eller formateringsåtergivning. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |

## Exempel

Visar hur man bevarar tomma rader när man laddar ett dokument.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Se även

* class [LoadOptions](../loadoptions/)
* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)
