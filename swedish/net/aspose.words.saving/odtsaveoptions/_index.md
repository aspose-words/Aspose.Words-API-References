---
title: OdtSaveOptions Class
linktitle: OdtSaveOptions
articleTitle: OdtSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.OdtSaveOptions för att förbättra din dokumentsparupplevelse. Anpassa inställningar för ODT/OTT-format och optimera ditt arbetsflöde!
type: docs
weight: 6110
url: /sv/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

Kan användas för att ange ytterligare alternativ när ett dokument sparas iOdt eller Ott format.

För att lära dig mer, besök[Ange alternativ för sparning](https://docs.aspose.com/words/net/specify-save-options/) dokumentationsartikel.

```csharp
public class OdtSaveOptions : SaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions/#constructor)() | Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iOdt format. |
| [OdtSaveOptions](odtsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iOdt eller Ott format. |
| [OdtSaveOptions](odtsaveoptions/#constructor_2)(*string*) | Initierar en ny instans av den här klassen som kan användas för att spara ett dokument iOdt format krypterad med ett lösenord. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger om inbäddning av teckensnitt med PostScript-konturer ska tillåtas när TrueType-teckensnitt bäddas in i ett dokument när det sparas. Standardvärdet är`falsk` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Hämtar eller ställer in en anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Hämtar eller anger sökvägen till standardmallen (inklusive filnamn). Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/odtsaveoptions/digitalsignaturedetails/) { get; set; } | Hämtar eller sätter[`DigitalSignatureDetails`](../digitalsignaturedetails/) objekt som används för att signera ett dokument. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur 3D-effekter renderas. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur DrawingML-former renderas. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | När`sann` , gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är`sann` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur bläckobjekt (InkML) renderas. |
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11/) { get; set; } | Anger om exporten ska överensstämma strikt med ODT-specifikation 1.1. OOo 3.0 visar filer korrekt när de innehåller element och attribut från ODT 1.2. Använd "false" för detta ändamål eller "sant" för strikt överensstämmelse med specifikation 1.1. Standardvärdet är`falsk` . |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit/) { get; set; } | Gör det möjligt att ange måttenheter som ska tillämpas på dokumentinnehåll. Standardvärdet ärCentimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Hämtar eller anger värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är`falsk` . |
| [Password](../../aspose.words.saving/odtsaveoptions/password/) { get; set; } | Hämtar eller ställer in ett lösenord för att kryptera dokument. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | När`sann` , pretty formats output där det är tillämpligt. Standardvärdet är`falsk` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Anropas när ett dokument sparas och accepterar data om sparningsförloppet. |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat/) { get; set; } | Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan varaOdt ellerOtt . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Anger mappen för temporära filer som används när man sparar till en DOC- eller DOCX-fil. Som standard är den här egenskapen`null` och inga temporära filer används. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Avgör om teckensnittsattributen ska ändras beroende på den teckenkod som används. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) egenskapen uppdateras innan den sparas. Standardvärdet är`falsk` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Hämtar eller anger ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är`sann` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) egenskapen uppdateras innan den sparas. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) egenskapen uppdateras innan den sparas. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Hämtar eller ställer in ett värde som avgör om antialiasing ska användas för rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Hämtar eller ställer in ett värde som avgör om högkvalitativa (dvs. långsamma) renderingsalgoritmer ska användas eller inte. |

## Anmärkningar

För närvarande tillhandahåller endast[`SaveFormat`](./saveformat/) egenskap, men i framtiden kommer andra alternativ att läggas till, till exempel ett krypteringslösenord eller inställningar för digitala signaturer.

## Exempel

Visar hur man får ett sparat dokument att överensstämma med ett äldre ODT-schema.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = OdtSaveMeasureUnit.Centimeters,
    IsStrictSchema11 = exportToOdt11Specs
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

Visar hur man använder olika måttenheter för att definiera stilparametrar för ett sparat ODT-dokument.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// När vi exporterar dokumentet till .odt kan vi använda ett OdtSaveOptions-objekt för att ändra hur vi sparar dokumentet.
// Vi kan ställa in egenskapen "MeasureUnit" till "OdtSaveMeasureUnit.Centimeters"
 // för att definiera innehåll såsom stilparametrar med hjälp av det metriska systemet, som Open Office använder.
// Vi kan ställa in egenskapen "MeasureUnit" till "OdtSaveMeasureUnit.Inches"
// för att definiera innehåll såsom stilparametrar med hjälp av det imperiala systemet, vilket Microsoft Word använder.
OdtSaveOptions saveOptions = new OdtSaveOptions
{
    MeasureUnit = odtSaveMeasureUnit
};

doc.Save(ArtifactsDir + "OdtSaveOptions.Odt11Schema.odt", saveOptions);
```

### Se även

* class [SaveOptions](../saveoptions/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
