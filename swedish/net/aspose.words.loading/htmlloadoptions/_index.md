---
title: HtmlLoadOptions Class
linktitle: HtmlLoadOptions
articleTitle: HtmlLoadOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.Loading.HtmlLoadOptions för att förbättra inläsningen av HTML-dokument i ett dokumentobjekt med anpassningsbara alternativ för optimal prestanda.
type: docs
weight: 4070
url: /sv/net/aspose.words.loading/htmlloadoptions/
---
## HtmlLoadOptions class

Gör det möjligt att ange ytterligare alternativ när HTML-dokument laddas in i en[`Document`](../../aspose.words/document/) objekt.

För att lära dig mer, besök[Ange laddningsalternativ](https://docs.aspose.com/words/net/specify-load-options/) dokumentationsartikel.

```csharp
public class HtmlLoadOptions : LoadOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [HtmlLoadOptions](htmlloadoptions/#constructor)() | Initierar en ny instans av den här klassen med standardvärden. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_2)(*string*) | En genväg för att initiera en ny instans av den här klassen med det angivna lösenordet för att läsa in ett krypterat dokument. |
| [HtmlLoadOptions](htmlloadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | En genväg för att initiera en ny instans av den här klassen med egenskaper inställda på de angivna värdena. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Hämtar eller ställer in strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er vid behov. Kan vara`null` eller tom sträng. Standard är`null` . |
| [BlockImportMode](../../aspose.words.loading/htmlloadoptions/blockimportmode/) { get; set; } | Hämtar eller ställer in ett värde som anger hur egenskaper för element på blocknivå importeras. Standardvärdet ärMerge . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Hämtar eller anger om metafil ska konverteras(Wmf ellerEmf ) bilder tillPngbildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Hämtar eller anger om former ska konverteras med EquationXML till Office Math-objekt. |
| [ConvertSvgToEmf](../../aspose.words.loading/htmlloadoptions/convertsvgtoemf/) { get; set; } | Hämtar eller ställer in ett värde som anger om inlästa SVG-bilder ska konverteras till EMF-format. Standardvärdet är`falsk` och, om möjligt, lagras inlästa SVG-bilder som de är utan konvertering. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Hämtar eller anger kodningen som ska användas för att läsa in ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad i dokumentet. Kan vara`null` Standard är`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Gör det möjligt att ange dokumentets teckensnittsinställningar. |
| [IgnoreNoscriptElements](../../aspose.words.loading/htmlloadoptions/ignorenoscriptelements/) { get; set; } | Hämtar eller anger ett värde som anger om &lt;noscript&gt; HTML-element ska ignoreras. Standardvärdet är`falsk` . |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Anger om OLE-data ska ignoreras. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Hämtar språkinställningar som kommer att användas när dokumentet laddas. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Anger formatet för det dokument som ska läsas in. Standard ärAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Gör det möjligt att ange att dokumentinläsningsprocessen ska matcha en specifik MS Word-version. Standardvärdet ärWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Hämtar eller ställer in lösenordet för att öppna ett krypterat dokument. Kan vara`null` eller tom sträng. Standard är`null` . |
| [PreferredControlType](../../aspose.words.loading/htmlloadoptions/preferredcontroltype/) { get; set; } | Hämtar eller ställer in önskad typ av dokumentnoder som representerar importerade &lt;input&gt;- och &lt;select&gt;-element. Standardvärdet ärFormField . |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Hämtar eller anger om fältet INCLUDEPICTURE ska bevaras vid läsning av Microsoft Word-format. Standardvärdet är`falsk` . |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Anropas under laddning av ett dokument och accepterar data om laddningsförloppet. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Gör det möjligt att styra hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [SupportFontFaceRules](../../aspose.words.loading/htmlloadoptions/supportfontfacerules/) { get; set; } | Hämtar eller ställer in ett värde som anger om @font-face-regler ska stödjas och om deklarerade teckensnitt ska läsas in. Standardvärdet är`falsk` . |
| [SupportVml](../../aspose.words.loading/htmlloadoptions/supportvml/) { get; set; } | Hämtar eller ställer in ett värde som anger om VML-avbildningar ska stödjas. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Tillåter användning av temporära filer vid läsning av dokument. Som standard är den här egenskapen`null` och inga temporära filer används. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Anger om fälten ska uppdateras med`smutsig` attribut. |
| [UseSystemLcid](../../aspose.words.loading/loadoptions/usesystemlcid/) { get; set; } | Hämtar eller anger om LCID-värde från Windows-registret ska användas för att bestämma standardmarginaler för sidinställningar. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Anropas under en inläsningsoperation, när ett problem upptäcks som kan leda till förlust av data- eller formateringsåtergivning. |
| [WebRequestTimeout](../../aspose.words.loading/htmlloadoptions/webrequesttimeout/) { get; set; } | Antalet millisekunder som ska väntas innan webbförfrågan går ut. Standardvärdet är 100000 millisekunder (100 sekunder). |

## Metoder

| namn | Beskrivning |
| --- | --- |
| override [Equals](../../aspose.words.loading/loadoptions/equals/)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |

## Exempel

Visar hur man stöder villkorsstyrda kommentarer när man laddar ett HTML-dokument.

```csharp
HtmlLoadOptions loadOptions = new HtmlLoadOptions();

// Om värdet är sant tar vi hänsyn till VML-kod när vi analyserar det inlästa dokumentet.
loadOptions.SupportVml = supportVml;

// Detta dokument innehåller en JPEG-bild inom taggarna "<!--[if gte vml 1]>",
// och en annan PNG-bild inom taggarna "<![if !vml]>".
// Om vi ställer in flaggan "SupportVml" till "true", så kommer Aspose.Words att ladda JPEG-filen.
// Om vi ställer in denna flagga till "false", kommer Aspose.Words bara att ladda PNG-filen.
Document doc = new Document(MyDir + "VML conditional.htm", loadOptions);

if (supportVml)
    Assert.AreEqual(ImageType.Jpeg, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
else
    Assert.AreEqual(ImageType.Png, ((Shape)doc.GetChild(NodeType.Shape, 0, true)).ImageData.ImageType);
```

### Se även

* class [LoadOptions](../loadoptions/)
* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)
