---
title: PdfSaveOptions
second_title: Aspose.Words för .NET API Referens
description: Kan användas för att ange ytterligare alternativ när du sparar ett dokument iPdf format.
type: docs
weight: 5240
url: /sv/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Kan användas för att ange ytterligare alternativ när du sparar ett dokument iPdf format.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions)() | Initierar en ny instans av denna klass som kan användas för att spara ett dokument i Pdf format. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning) { get; set; } | En flagga som anger om ytterligare textpositioneringsoperatorer ska skrivas eller inte. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar om man ska tillåta inbäddning av teckensnitt med PostScript outlines när inbäddning av TrueType-teckensnitt i ett dokument på det sparas. Standardvärdet är **falsk** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur färger återges. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance) { get; set; } | Anger överensstämmelsenivån för PDF-standarder för utdatadokument. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks) { get; set; } | Anger om fotnots-/slutnotsreferenser i huvudtextartikeln ska konverteras till aktiva hyperlänkar. När den klickas leder hyperlänken till motsvarande fotnot/slutnot. Standard är`falsk` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport) { get; set; } | Hämtar eller ställer in ett värde som bestämmer vägen[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties) exporteras till PDF-fil. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Hämtar eller ställer in anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Hämtar eller ställer in sökvägen till standardmall (inklusive filnamn). Standardvärdet för den här egenskapen är **tom sträng** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails) { get; set; } | Hämtar eller ställer in detaljerna för att signera PDF-dokumentet. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle) { get; set; } | En flagga som anger om fönstrets namnlist ska visa dokumenttiteln hämtad från titelposten i dokumentinformationslexikonet. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur 3D-effekter renderas. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur DrawingML-former renderas. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions) { get; set; } | Gör det möjligt att ange alternativ för nedsampling. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts) { get; set; } | Styr hur teckensnitt bäddas in i de resulterande PDF-dokumenten. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails) { get; set; } | Hämtar eller ställer in detaljerna för kryptering av PDF-dokumentet. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure) { get; set; } | Hämtar eller ställer in ett värde som avgör om dokumentstruktur ska exporteras eller inte. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | När sant, gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är **Sann** . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag) { get; set; } | Hämtar eller ställer in ett värde som avgör om en "Span"-tagg ska skapas eller inte i dokumentstrukturen för att exportera textspråket. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Hämtar eller ställer in värde som avgör vilka dokumentformat som tillåts mappas av[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Endast som standardFlatOpc dokumentformat får mappas. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode) { get; set; } | Anger typsnittets inbäddningsläge. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode) { get; set; } | Bestämmer hur bokmärken i sidhuvuden/sidfötter exporteras. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode) { get; set; } | Anger hur färgrymden kommer att väljas för bilderna i PDF-dokument. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression) { get; set; } | Anger komprimeringstyp som ska användas för alla bilder i dokumentet. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur bläckobjekt (InkML) renderas. |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages) { get; set; } | En flagga som indikerar om bildinterpolation ska utföras av en överensstämmande läsare. När`falsk` anges, skrivs inte flaggan till utdatadokumentet och standardbeteendet för läsaren används istället. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality) { get; set; } | Hämtar eller ställer in ett värde som bestämmer kvaliteten på JPEG-bilderna i PDF-dokumentet. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Hämtar eller ställer in värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är **falsk** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | Tillåter att ange alternativ för metafilrendering. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | Hämtar eller sätter[`NumeralFormat`](../numeralformat) används för återgivning av siffror. Europeiska siffror används som standard. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow) { get; set; } | Hämtar eller ställer in ett värde som avgör om hyperlänkar i utdata Pdf document tvingas öppnas i ett nytt fönster (eller flik) i en webbläsare. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput) { get; set; } | Flagga indikerar om det krävs för att optimera utdata. Om denna flagga ställs in redundanta kapslade dukar och tomma dukar tas bort, sammanlänkas även grannglyfer med samma formatering. Obs! Noggrannheten i innehållsvisningen kan påverkas den här egenskapen är inställd på true. Standard är false. |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions) { get; } | Gör det möjligt att ange konturalternativ. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode) { get; set; } | Anger hur PDF-dokumentet ska visas när det öppnas i PDF-läsaren. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | Gör det möjligt att styra hur separata sidor sparas när ett dokument exporteras till fast sidformat. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | Hämtar eller ställer in sidorna att rendera. Standard är alla sidor i dokumentet. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages) { get; set; } | Hämtar eller ställer in ett värde som bestämmer om transparenta bilder ska förblandas med svart bakgrundsfärg. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields) { get; set; } | Anger om Microsoft Word-formulärfält ska bevaras som formulärfält i PDF eller konvertera dem till text. Standard är`falsk` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | När`Sann` , snygga format utdata där tillämpligt. Standardvärdet är **falsk** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Anropas när ett dokument sparas och accepterar data om lagringsförlopp. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat) { get; set; } | Anger formatet som dokumentet kommer att sparas i om detta sparaalternativ-objekt används. Kan endastPdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Anger mappen för temporära filer som används när du sparar till en DOC- eller DOCX-fil. Som standard är denna egenskap`null` och inga temporära filer används. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression) { get; set; } | Anger komprimeringstyp som ska användas för allt textinnehåll i dokumentet. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) egenskapen uppdateras innan du sparar. Standardvärdet är falskt; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Hämtar eller ställer in ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är **Sann** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) egenskapen uppdateras innan du sparar. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) egenskapen uppdateras innan du sparar. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Hämtar eller ställer in värde som avgör om innehållet i[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) uppdateras innan du sparar. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Hämtar eller ställer in ett värde som avgör om kantutjämning ska användas eller inte för rendering. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings) { get; set; } | Hämtar eller ställer in ett booleskt värde som indikerar om dokumentet ska sparas med en layout för häftesutskrift, om det anges via[`MultiplePages`](../../aspose.words/pagesetup/multiplepages) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts) { get; set; } | Hämtar eller ställer in ett värde som avgör om TrueType-teckensnitten Arial, Times New Roman, Courier New och Symbol ska ersättas med kärn-PDF Type 1-teckensnitt. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Hämtar eller ställer in ett värde som avgör huruvida högkvalitativa (dvs långsamma) renderingsalgoritmer ska användas eller inte. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior) { get; set; } | Hämtar eller ställer in ett värde som bestämmer vilken typ av zoom som ska användas när ett dokument öppnas med en PDF-visare. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor) { get; set; } | Hämtar eller ställer in ett värde som bestämmer zoomfaktor (i procent) för ett dokument. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone)() | Skapar en djup klon av detta objekt. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | Bestämmer om det angivna objektet har samma värde som det aktuella objektet. |

### Exempel

Visar hur du ändrar bildfärg med egenskapen sparalternativ.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
// Ställ in egenskapen "ColorMode" till "Gråskala" för att återge alla bilder från dokumentet i svartvitt.
// Storleken på utdatadokumentet kan vara större med den här inställningen.
// Ställ in egenskapen "ColorMode" till "Normal" för att återge alla bilder i färg.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

Visar hur du använder textkomprimering när du sparar ett dokument till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "TextCompression" till "PdfTextCompression.None" för att inte tillämpa någon
// komprimering till text när vi sparar dokumentet till PDF.
// Ställ in egenskapen "TextCompression" till "PdfTextCompression.Flate" för att tillämpa ZIP-komprimering
// till text när vi sparar dokumentet till PDF. Ju större dokument, desto större inverkan kommer detta att ha.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Visar hur man konverterar ett helt dokument till PDF med tre nivåer i dokumentöversikten.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker för nivåerna 1 till 5.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;

builder.Writeln("Heading 1.2.2.1");
builder.Writeln("Heading 1.2.2.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading5;

builder.Writeln("Heading 1.2.2.2.1");
builder.Writeln("Heading 1.2.2.2.2");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Spara"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Det utgående PDF-dokumentet kommer att innehålla en disposition, som är en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Genom att klicka på en post i denna disposition kommer vi till platsen för dess respektive rubrik.
// Ställ in egenskapen "HeadingsOutlineLevels" till "4" för att utesluta alla rubriker vars nivåer är över 4 från dispositionen.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Om en konturpost har efterföljande poster på en högre nivå mellan sig och nästa post på samma eller lägre nivå,
// en pil visas till vänster om posten. Denna post är "ägare" till flera sådana "underposter".
// I vårt dokument är dispositionsposterna från den 5:e rubriknivån underposter till den andra 4:e nivåns dispositionspost,
  // posterna på 4:e och 5:e rubriknivån är underposter till den andra 3:e nivåposten, och så vidare.
// I dispositionen kan vi klicka på pilen för "ägare"-posten för att komprimera/expandera alla dess underposter.
// Ställ in egenskapen "ExpandedOutlineLevels" till "2" för att automatiskt utöka alla rubriknivå 2 och lägre dispositionsposter
 // och kollapsa alla nivåer och 3 och högre poster när vi öppnar dokumentet.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Se även

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving)
* hopsättning [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
