---
title: TxtLoadOptions
second_title: Aspose.Words för .NET API Referens
description: Tillåter att ange ytterligare alternativ vid laddningText dokument till enDocument../aspose.words/document objekt.
type: docs
weight: 3530
url: /sv/net/aspose.words.loading/txtloadoptions/
---
## TxtLoadOptions class

Tillåter att ange ytterligare alternativ vid laddningText dokument till en[`Document`](../../aspose.words/document) objekt.

```csharp
public class TxtLoadOptions : LoadOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [TxtLoadOptions](txtloadoptions)() | Initierar en ny instans av denna klass med standardvärden. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [BaseUri](../../aspose.words.loading/loadoptions/baseuri) { get; set; } | Hämtar eller ställer in strängen som ska användas för att lösa relativa URI:er som finns i dokumentet till absoluta URI:er vid behov. Kan vara null eller tom sträng. Standard är null. |
| [ConvertMetafilesToPng](../../aspose.words.loading/loadoptions/convertmetafilestopng) { get; set; } | Hämtar eller ställer in om metafil ska konverteras (Wmf ellerEmf ) bilder tillPng bildformat. |
| [ConvertShapeToOfficeMath](../../aspose.words.loading/loadoptions/convertshapetoofficemath) { get; set; } | Hämtar eller ställer in om former ska konverteras med EquationXML till Office Math-objekt. |
| [DetectNumberingWithWhitespaces](../../aspose.words.loading/txtloadoptions/detectnumberingwithwhitespaces) { get; set; } | Gör det möjligt att ange hur numrerade listobjekt ska kännas igen när dokument importeras från vanligt textformat. Standardvärdet är sant. |
| [DocumentDirection](../../aspose.words.loading/txtloadoptions/documentdirection) { get; set; } | Hämtar eller ställer in en dokumentriktning. Standardvärdet ärLeftToRight . |
| [Encoding](../../aspose.words.loading/loadoptions/encoding) { get; set; } | Hämtar eller ställer in kodningen som ska användas för att ladda ett HTML-, TXT- eller CHM-dokument om kodningen inte är specificerad inuti dokumentet. Kan vara null. Standard är null. |
| [FlatOpcXmlMappingOnly](../../aspose.words.loading/loadoptions/flatopcxmlmappingonly) { get; set; } | Hämtar eller ställer in värde som avgör vilka dokumentformat som tillåts mappas av[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Endast som standardFlatOpc dokumentformat får mappas. |
| [FontSettings](../../aspose.words.loading/loadoptions/fontsettings) { get; set; } | Gör det möjligt att ange inställningar för dokumentteckensnitt. |
| [LanguagePreferences](../../aspose.words.loading/loadoptions/languagepreferences) { get; } | Får språkinställningar som kommer att användas när dokumentet laddas. |
| [LeadingSpacesOptions](../../aspose.words.loading/txtloadoptions/leadingspacesoptions) { get; set; } | Hämtar eller ställer in föredraget alternativ för en ledande utrymmeshantering. Standardvärdet ärConvertToIndent . |
| [LoadFormat](../../aspose.words.loading/loadoptions/loadformat) { get; set; } | Anger formatet på dokumentet som ska laddas. Standard ärAuto . |
| [MswVersion](../../aspose.words.loading/loadoptions/mswversion) { get; set; } | Tillåter att ange att dokumentladdningsprocessen ska matcha en specifik MS Word-version. Standardvärdet ärWord2019 |
| [Password](../../aspose.words.loading/loadoptions/password) { get; set; } | Hämtar eller ställer in lösenordet för att öppna ett krypterat dokument. Kan vara null eller tom sträng. Standard är null. |
| [PreserveIncludePictureField](../../aspose.words.loading/loadoptions/preserveincludepicturefield) { get; set; } | Hämtar eller ställer in om fältet INCLUDEPICTURE ska bevaras vid läsning av Microsoft Word-format. Standardvärdet är false. |
| [ProgressCallback](../../aspose.words.loading/loadoptions/progresscallback) { get; set; } | Anropas under laddning av ett dokument och accepterar data om laddningsförlopp. |
| [ResourceLoadingCallback](../../aspose.words.loading/loadoptions/resourceloadingcallback) { get; set; } | Gör det möjligt att styra hur externa resurser (bilder, stilmallar) laddas när ett dokument importeras från HTML, MHTML. |
| [TempFolder](../../aspose.words.loading/loadoptions/tempfolder) { get; set; } | Tillåter att använda temporära filer vid läsning av dokument. Som standard är denna egenskap`null` och inga temporära filer används. |
| [TrailingSpacesOptions](../../aspose.words.loading/txtloadoptions/trailingspacesoptions) { get; set; } | Hämtar eller ställer in föredraget alternativ för en efterföljande utrymmeshantering. Standardvärdet ärTrim . |
| [UpdateDirtyFields](../../aspose.words.loading/loadoptions/updatedirtyfields) { get; set; } | Anger om fälten ska uppdateras med`smutsig` attribut. |
| [WarningCallback](../../aspose.words.loading/loadoptions/warningcallback) { get; set; } | Anropas under en laddningsoperation, när ett problem upptäcks som kan resultera i förlust av data eller formatering. |

### Se även

* class [LoadOptions](../loadoptions)
* namnutrymme [Aspose.Words.Loading](../../aspose.words.loading)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
