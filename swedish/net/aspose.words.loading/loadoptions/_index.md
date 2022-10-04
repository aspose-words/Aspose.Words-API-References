---
title: LoadOptions
second_title: Aspose.Words för .NET API Referens
description: Gör det möjligt att ange ytterligare alternativ som lösenord eller basURI när laddar ett dokument i enDocument../aspose.words/document/ objekt.
type: docs
weight: 3460
url: /sv/net/aspose.words.loading/loadoptions/
---
## LoadOptions class

Gör det möjligt att ange ytterligare alternativ (som lösenord eller bas-URI) när laddar ett dokument i en[`Document`](../../aspose.words/document/) objekt.

```csharp
public class LoadOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [LoadOptions](loadoptions/#constructor)() | Initierar en ny instans av denna klass med standardvärden. |
| [LoadOptions](loadoptions/#constructor_2)(string) | En genväg för att initiera en ny instans av denna klass med det angivna lösenordet för att ladda ett krypterat dokument. |
| [LoadOptions](loadoptions/#constructor_1)(LoadFormat, string, string) | En genväg för att initiera en ny instans av denna klass med egenskaper inställda på de angivna värdena. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri/) { get; set; } | Hämtar eller ställer in strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er vid behov. Kan vara null eller tom sträng. Standard är null. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng/) { get; set; } | Hämtar eller ställer in om metafil ska konverteras (Wmf ellerEmf ) bilder tillPng bildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath/) { get; set; } | Hämtar eller ställer in om former ska konverteras med EquationXML till Office Math-objekt. |
| [Encoding](../../aspose.words.loading/loadoptions/encoding/) { get; set; } | Hämtar eller ställer in kodningen som ska användas för att ladda ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad inuti dokumentet. Kan vara null. Standard är null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly/) { get; set; } | Hämtar eller ställer in värde som avgör vilka dokumentformat som tillåts mappas av[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Endast som standardFlatOpc dokumentformat får mappas. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings/) { get; set; } | Gör det möjligt att ange inställningar för dokumentteckensnitt. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences/) { get; } | Får språkinställningar som kommer att användas när dokumentet laddas. |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat/) { get; set; } | Anger formatet på dokumentet som ska laddas. Standard ärAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion/) { get; set; } | Tillåter att ange att dokumentladdningsprocessen ska matcha en specifik MS Word-version. Standardvärdet ärWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password/) { get; set; } | Hämtar eller ställer in lösenordet för att öppna ett krypterat dokument. Kan vara null eller tom sträng. Standard är null. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield/) { get; set; } | Hämtar eller ställer in om fältet INCLUDEPICTURE ska bevaras vid läsning av Microsoft Word-format. Standardvärdet är false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback/) { get; set; } | Anropas under laddning av ett dokument och accepterar data om laddningsförlopp. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback/) { get; set; } | Gör det möjligt att styra hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder/) { get; set; } | Tillåter att använda temporära filer vid läsning av dokument. Som standard är denna egenskap`null` och inga temporära filer används. |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields/) { get; set; } | Anger om fälten ska uppdateras med`smutsig` attribut. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback/) { get; set; } | Anropas under en laddningsoperation, när ett problem upptäcks som kan resultera i förlust av data eller formatering. |

### Exempel

Visar hur man laddar ett krypterat Microsoft Word-dokument.

```csharp
Document doc;

// Aspose.Words ger ett undantag om vi försöker öppna ett krypterat dokument utan dess lösenord.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(MyDir + "Encrypted.docx"));

// När ett sådant dokument laddas skickas lösenordet till dokumentets konstruktor med hjälp av ett LoadOptions-objekt.
LoadOptions options = new LoadOptions("docPassword");

// Det finns två sätt att ladda ett krypterat dokument med ett LoadOptions-objekt.
// 1 - Ladda dokumentet från det lokala filsystemet efter filnamn:
doc = new Document(MyDir + "Encrypted.docx", options);
// 2 - Ladda dokumentet från en ström:
using (Stream stream = File.OpenRead(MyDir + "Encrypted.docx"))
{
    doc = new Document(stream, options);
```

### Se även

* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
