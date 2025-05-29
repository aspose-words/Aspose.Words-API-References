---
title: LoadOptions Class
linktitle: LoadOptions
articleTitle: LoadOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.LoadOptions för förbättrad dokumentinläsning. Ställ in lösenord och bas-URI:er enkelt för sömlös integration och säkerhet.
type: docs
weight: 4110
url: /sv/net/aspose.words.loading/loadoptions/
---
## LoadOptions class

Gör det möjligt att ange ytterligare alternativ (som lösenord eller bas-URI) när ett dokument laddas in i en[`Document`](../../aspose.words/document/) objekt.

För att lära dig mer, besök[Ange laddningsalternativ](https://docs.aspose.com/words/net/specify-load-options/) dokumentationsartikel.

```csharp
public class LoadOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [LoadOptions](loadoptions/#constructor)() | Initierar en ny instans av den här klassen med standardvärden. |
| [LoadOptions](loadoptions/#constructor_2)(*string*) | En genväg för att initiera en ny instans av den här klassen med det angivna lösenordet för att läsa in ett krypterat dokument. |
| [LoadOptions](loadoptions/#constructor_1)(*[LoadFormat](../../aspose.words/loadformat/), string, string*) | En genväg för att initiera en ny instans av den här klassen med egenskaper inställda på de angivna värdena. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Hämtar eller ställer in strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er vid behov. Kan vara`null` eller tom sträng. Standard är`null` . |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Hämtar eller anger om metafil ska konverteras(Wmf ellerEmf ) bilder tillPngbildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Hämtar eller anger om former ska konverteras med EquationXML till Office Math-objekt. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Hämtar eller anger kodningen som ska användas för att läsa in ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad i dokumentet. Kan vara`null` Standard är`null` . |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Gör det möjligt att ange dokumentets teckensnittsinställningar. |
| [IgnoreOleData](../../aspose.words.loading/loadoptions/ignoreoledata/) { get; set; } | Anger om OLE-data ska ignoreras. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Hämtar språkinställningar som kommer att användas när dokumentet laddas. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Anger formatet för det dokument som ska läsas in. Standard ärAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Gör det möjligt att ange att dokumentinläsningsprocessen ska matcha en specifik MS Word-version. Standardvärdet ärWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Hämtar eller ställer in lösenordet för att öppna ett krypterat dokument. Kan vara`null` eller tom sträng. Standard är`null` . |
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

Visar hur man laddar ett krypterat Microsoft Word-dokument.

```csharp
Document doc;

// Aspose.Words utlöser ett undantag om vi försöker öppna ett krypterat dokument utan dess lösenord.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// När ett sådant dokument laddas skickas lösenordet till dokumentets konstruktor med hjälp av ett LoadOptions-objekt.
LoadOptions options = new LoadOptions("docPassword");

// Det finns två sätt att läsa in ett krypterat dokument med ett LoadOptions-objekt.
// 1 - Ladda dokumentet från det lokala filsystemet med filnamn:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Ladda dokumentet från en ström:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
}
```

### Se även

* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)
