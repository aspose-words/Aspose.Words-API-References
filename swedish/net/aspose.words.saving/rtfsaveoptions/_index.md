---
title: RtfSaveOptions
second_title: Aspose.Words för .NET API Referens
description: Kan användas för att ange ytterligare alternativ när du sparar ett dokument iRtf format.
type: docs
weight: 5290
url: /sv/net/aspose.words.saving/rtfsaveoptions/
---
## RtfSaveOptions class

Kan användas för att ange ytterligare alternativ när du sparar ett dokument iRtf format.

```csharp
public class RtfSaveOptions : SaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [RtfSaveOptions](rtfsaveoptions)() | Default_Constructor |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar om man ska tillåta inbäddning av teckensnitt med PostScript outlines när inbäddning av TrueType-teckensnitt i ett dokument på det sparas. Standardvärdet är **falsk** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Hämtar eller ställer in anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Hämtar eller ställer in sökvägen till standardmall (inklusive filnamn). Standardvärdet för den här egenskapen är **tom sträng** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur 3D-effekter renderas. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-former renderas. |
| [ExportCompactSize](../../aspose.words.saving/rtfsaveoptions/exportcompactsize) { get; set; } | Gör det möjligt att göra utmatade RTF-dokument mindre i storlek, men om de innehåller RTL (höger-till-vänster) text kommer den inte att visas korrekt. Standardvärdet är`falsk` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | När sant, gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är **Sann** . |
| [ExportImagesForOldReaders](../../aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders) { get; set; } | Anger om nyckelorden för "gamla läsare" skrivs till RTF eller inte. Detta kan avsevärt påverka storleken på RTF-dokumentet. Standardvärdet är`Sann` . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Hämtar eller ställer in värde som avgör vilka dokumentformat som tillåts mappas av[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Endast som standardFlatOpc dokumentformat får mappas. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur bläckobjekt (InkML) renderas. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Hämtar eller ställer in värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är **falsk** . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | När`Sann` , snygga format utdata där tillämpligt. Standardvärdet är **falsk** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Anropas när ett dokument sparas och accepterar data om lagringsförlopp. |
| override [SaveFormat](../../aspose.words.saving/rtfsaveoptions/saveformat) { get; set; } | Anger formatet som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan endastRtf . |
| [SaveImagesAsWmf](../../aspose.words.saving/rtfsaveoptions/saveimagesaswmf) { get; set; } | När sant kommer alla bilder att sparas som WMF. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Anger mappen för temporära filer som används när du sparar till en DOC- eller DOCX-fil. Som standard är denna egenskap`null` och inga temporära filer används. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) egenskapen uppdateras innan du sparar. Standardvärdet är falskt; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Hämtar eller ställer in ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är **Sann** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) egenskapen uppdateras innan du sparar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) egenskapen uppdateras innan du sparar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Hämtar eller ställer in värde som avgör om innehållet i[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) uppdateras innan du sparar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Hämtar eller ställer in ett värde som avgör om kantutjämning ska användas eller inte för rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Hämtar eller ställer in ett värde som avgör huruvida högkvalitativa (dvs långsamma) renderingsalgoritmer ska användas eller inte. |

### Exempel

Visar hur man sparar ett dokument till .rtf med anpassade alternativ.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Skapa ett "RtfSaveOptions"-objekt för att skicka till dokumentets "Save"-metod för att ändra hur vi sparar det till en RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Ställ in egenskapen "ExportCompactSize" till "true" till
// minska storleken på det sparade dokumentet på bekostnad av höger-till-vänster-textkompatibilitet.
options.ExportCompactSize = true;

// Ställ in egenskapen "ExportImagesFotOldReaders" till "true" för att använda extra nyckelord för att säkerställa att vårt dokument är
// kompatibel med pre-Microsoft Word 97 läsare och WordPad.
// Ställ in egenskapen "ExportImagesFotOldReaders" till "false" för att minska storleken på dokumentet,
// men hindra gamla läsare från att kunna läsa eventuella icke-metafiler eller BMP-bilder som dokumentet kan innehålla.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Se även

* class [SaveOptions](../saveoptions)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
