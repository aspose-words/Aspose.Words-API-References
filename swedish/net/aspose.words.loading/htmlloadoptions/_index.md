---
title: Class HtmlLoadOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Loading.HtmlLoadOptions klass. Gör det möjligt att ange ytterligare alternativ när HTMLdokument läses in i enDocument objekt.
type: docs
weight: 3620
url: /sv/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Gör det möjligt att ange ytterligare alternativ när HTML-dokument läses in i en[`Document`](../../aspose.words/document/) objekt.

För att lära dig mer, besök[Ange laddningsalternativ](https://docs.aspose.com/words/net/specify-load-options/) dokumentationsartikel.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Initierar en ny instans av denna klass med standardvärden. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(string) | En genväg för att initiera en ny instans av denna klass med det angivna lösenordet för att ladda ett krypterat dokument. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(LoadFormat, string, string) | En genväg för att initiera en ny instans av denna klass med egenskaper inställda på de angivna värdena. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Hämtar eller ställer in strängen som kommer att användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er vid behov. Kan vara`null` eller tom sträng. Standard är`null` . |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Hämtar eller ställer in ett värde som anger hur egenskaper för element på blocknivå importeras. Standardvärdet ärMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Hämtar eller ställer in om metafil ska konverteras (Wmf ellerEmf ) bilder tillPng bildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Hämtar eller ställer in om former ska konverteras med EquationXML till Office Math-objekt. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Hämtar eller ställer in ett värde som anger om laddade SVG-bilder ska konverteras till EMF-formatet. Standardvärdet är`falsk` och om möjligt lagras inlästa SVG-bilder som de är utan konvertering. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Hämtar eller ställer in kodningen som ska användas för att ladda ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad inuti dokumentet. Kan vara`null` . Standard är`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Gör det möjligt att ange inställningar för dokumentteckensnitt. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | Hämtar eller ställer in ett värde som anger om &lt;noscript&gt; HTML-element ska ignoreras. Standardvärdet är`falsk` . |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Anger om OLE-data ska ignoreras. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Får språkinställningar som kommer att användas när dokumentet laddas. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Anger formatet på dokumentet som ska laddas. Standard ärAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Tillåter att ange att dokumentladdningsprocessen ska matcha en specifik MS Word-version. Standardvärdet ärWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Hämtar eller ställer in lösenordet för att öppna ett krypterat dokument. Kan vara`null` eller tom sträng. Standard är`null` . |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | Hämtar eller ställer in önskad typ av dokumentnoder som kommer att representera importerade &lt;input&gt; och &lt;select&gt; element. Standardvärdet ärFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Hämtar eller ställer in om fältet INCLUDEPICTURE ska bevaras vid läsning av Microsoft Word-format. Standardvärdet är`falsk` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Anropas under laddning av ett dokument och accepterar data om laddningsförlopp. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Gör det möjligt att styra hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | Hämtar eller ställer in ett värde som anger om VML-bilder ska stödjas. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Tillåter att använda temporära filer vid läsning av dokument. Som standard är denna egenskap`null` och inga temporära filer används. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Anger om fälten ska uppdateras med`smutsig` attribut. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Anropas under en laddningsoperation, när ett problem upptäcks som kan resultera i förlust av data eller formatering. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Antalet millisekunder som ska vänta innan webbförfrågan timeout. Standardvärdet är 100 000 millisekunder (100 sekunder). |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(object) |  |

### Se även

* class [LoadOptions](../loadoptions/)
* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)


