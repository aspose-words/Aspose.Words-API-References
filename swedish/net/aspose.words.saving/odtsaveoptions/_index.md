---
title: Class OdtSaveOptions
second_title: Aspose.Words för .NET API Referens
description: Aspose.Words.Saving.OdtSaveOptions klass. Kan användas för att ange ytterligare alternativ när du sparar ett dokument iOdt or Ott format.
type: docs
weight: 5050
url: /sv/net/aspose.words.saving/odtsaveoptions/
---
## OdtSaveOptions class

Kan användas för att ange ytterligare alternativ när du sparar ett dokument iOdt or Ott format.

```csharp
public class OdtSaveOptions : SaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [OdtSaveOptions](odtsaveoptions/#constructor)() | Initierar en ny instans av denna klass som kan användas för att spara ett dokument iOdt format. |
| [OdtSaveOptions](odtsaveoptions/#constructor_1)(SaveFormat) | Initierar en ny instans av denna klass som kan användas för att spara ett dokument iOdt or Ott format. |
| [OdtSaveOptions](odtsaveoptions/#constructor_2)(string) | Initierar en ny instans av denna klass som kan användas för att spara ett dokument iOdt format krypterad med ett lösenord. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar om man ska tillåta inbäddning av teckensnitt med PostScript outlines när inbäddning av TrueType-teckensnitt i ett dokument på det sparas. Standardvärdet är **falsk** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Hämtar eller ställer in anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Hämtar eller ställer in sökvägen till standardmall (inklusive filnamn). Standardvärdet för den här egenskapen är **tom sträng** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur 3D-effekter renderas. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-former renderas. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | När sant, gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är **Sann** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Hämtar eller ställer in värde som avgör vilka dokumentformat som tillåts mappas av[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Endast som standardFlatOpc dokumentformat får mappas. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur bläckobjekt (InkML) renderas. |
| [IsStrictSchema11](../../aspose.words.saving/odtsaveoptions/isstrictschema11/) { get; set; } | Anger om export ska motsvara ODT-specifikation 1.1 strikt. OOo 3.0 visar filer korrekt när de innehåller element och attribut för ODT 1.2. Använd "false" för detta ändamål, eller "true" för strikt överensstämmelse med specifikation 1.1. Standardvärdet är **falsk** . |
| [MeasureUnit](../../aspose.words.saving/odtsaveoptions/measureunit/) { get; set; } | Tillåter att ange måttenheter som ska tillämpas på dokumentinnehåll. Standardvärdet ärCentimeters |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Hämtar eller ställer in värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är **falsk** . |
| [Password](../../aspose.words.saving/odtsaveoptions/password/) { get; set; } | Hämtar eller ställer in ett lösenord för att kryptera dokument. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | När`Sann` , snygga format utdata där tillämpligt. Standardvärdet är **falsk** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Anropas när ett dokument sparas och accepterar data om lagringsförlopp. |
| override [SaveFormat](../../aspose.words.saving/odtsaveoptions/saveformat/) { get; set; } | Anger formatet som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan varaOdt ellerOtt . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Anger mappen för temporära filer som används när du sparar till en DOC- eller DOCX-fil. Som standard är denna egenskap`null` och inga temporära filer används. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) egenskapen uppdateras innan du sparar. Standardvärdet är falskt; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Hämtar eller ställer in ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är **Sann** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) egenskapen uppdateras innan du sparar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) egenskapen uppdateras innan du sparar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Hämtar eller ställer in värde som avgör om innehållet i[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) uppdateras innan du sparar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Hämtar eller ställer in ett värde som avgör om kantutjämning ska användas eller inte för rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Hämtar eller ställer in ett värde som avgör huruvida högkvalitativa (dvs långsamma) renderingsalgoritmer ska användas eller inte. |

### Anmärkningar

För närvarande ger endast[`SaveFormat`](./saveformat/) egendom, men i framtiden kommer att läggas till andra alternativ, såsom ett krypteringslösenord eller inställningar för digitala signaturer.

### Exempel

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
// för att definiera innehåll som stilparametrar med hjälp av det metriska systemet, som Open Office använder. 
// Vi kan ställa in egenskapen "MeasureUnit" till "OdtSaveMeasureUnit.Inches"
// för att definiera innehåll som stilparametrar med hjälp av det imperialistiska systemet, som Microsoft Word använder.
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


