---
title: PdfSaveOptions Class
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words för .NET
description: Upptäck Aspose.Words.PdfSaveOptions för att förbättra din dokumentsparupplevelse. Anpassa inställningarna för optimal PDF-utskriftskvalitet och prestanda.
type: docs
weight: 6320
url: /sv/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Kan användas för att ange ytterligare alternativ när ett dokument sparas iPdf format.

För att lära dig mer, besök[Ange alternativ för sparning](https://docs.aspose.com/words/net/specify-save-options/) dokumentationsartikel.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Konstruktörer

| namn | Beskrivning |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | Initierar en ny instans av den här klassen som kan användas för att spara ett dokument i Pdf format. |

## Egenskaper

| namn | Beskrivning |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | En flagga som anger om ytterligare textpositioneringsoperatorer ska skrivas eller inte. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Hämtar eller ställer in ett booleskt värde som anger om inbäddning av teckensnitt med PostScript-konturer ska tillåtas när TrueType-teckensnitt bäddas in i ett dokument när det sparas. Standardvärdet är`falsk` . |
| [AttachmentsEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/) { get; set; } | Hämtar eller anger ett värde som avgör hur bilagor bäddas in i PDF-dokumentet. |
| [CacheBackgroundGraphics](../../aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/) { get; set; } | Hämtar eller anger ett värde som avgör om grafik som placeras i dokumentets bakgrund ska cachelagras eller inte. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur färger återges. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | Anger efterlevnadsnivån för PDF-standarder för utdatadokument. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | Anger om fotnots-/slutnotsreferenser i huvudtextartikeln ska konverteras till aktiva hyperlänkar. När hyperlänken klickas leder den till motsvarande fotnot/slutnot. Standard är`falsk` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer hur[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) exporteras till PDF-fil. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Hämtar eller ställer in en anpassad lokal tidszon som används för datum-/tidsfält. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Hämtar eller anger sökvägen till standardmallen (inklusive filnamn). Standardvärdet för den här egenskapen är**tom sträng** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | Hämtar eller anger detaljerna för att signera PDF-dokumentet. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | En flagga som anger om fönstrets titelrad ska visa dokumenttiteln hämtad från titelposten i dokumentinformationsordlistan. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur 3D-effekter renderas. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur DrawingML-effekter renderas. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur DrawingML-former renderas. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | Gör det möjligt att ange nedprovningsalternativ. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | Styr hur teckensnitt bäddas in i de resulterande PDF-dokumenten. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | Hämtar eller anger detaljerna för kryptering av PDF-dokumentet. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | Hämtar eller anger ett värde som avgör om dokumentstrukturen ska exporteras eller inte. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | När`sann` , gör att namnet och versionen av Aspose.Words bäddas in i producerade filer. Standardvärdet är`sann` . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | Hämtar eller anger ett värde som avgör om en "Span"-tagg ska skapas i dokumentstrukturen för att exportera textspråket. |
| [ExportParagraphGraphicsToArtifact](../../aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/) { get; set; } | Hämtar eller anger ett värde som avgör om en styckegrafik ska markeras som en artefakt. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | Anger inbäddningsläget för teckensnitt. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | Bestämmer hur bokmärken i sidhuvuden/sidfot exporteras. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | Anger hur färgrymden ska väljas för bilderna i PDF-dokumentet. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | Anger komprimeringstyp som ska användas för alla bilder i dokumentet. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Hämtar eller ställer in ett värde som avgör hur bläckobjekt (InkML) renderas. |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | En flagga som anger om bildinterpolering ska utföras av en kompatibel läsare. När`falsk` är specificerad, skrivs inte flaggan till utdatadokumentet och används läsarens standardbeteende istället. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | Hämtar eller ställer in ett värde som avgör kvaliteten på JPEG-bilderna i PDF-dokumentet. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Hämtar eller anger värde som avgör om minnesoptimering ska utföras innan dokumentet sparas. Standardvärdet för den här egenskapen är`falsk` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Gör det möjligt att ange renderingsalternativ för metafiler. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Hämtar eller sätter[`NumeralFormat`](../numeralformat/) används för rendering av siffror. Europeiska siffror används som standard. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | Hämtar eller anger ett värde som avgör om hyperlänkar i PDF-dokumentet tvingas öppnas i ett nytt fönster (eller en ny flik) i en webbläsare. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Flaggan anger om det är nödvändigt att optimera utdata. Om denna flagga är inställd tas redundanta kapslade arbetsytor och tomma arbetsytor bort, sammanfogas även angränsande tecken med samma formatering. Obs! Noggrannheten i innehållsvisningen kan påverkas om den här egenskapen är inställd på`sann` . Standard är`falsk` . |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | Gör det möjligt att ange dispositionsalternativ. |
| [PageLayout](../../aspose.words.saving/pdfsaveoptions/pagelayout/) { get; set; } | Anger vilken sidlayout som ska användas när dokumentet öppnas i en PDF-läsare. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | Anger hur PDF-dokumentet ska visas när det öppnas i en PDF-läsare. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Gör det möjligt att styra hur separata sidor sparas när ett dokument exporteras till ett fast sidformat. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Hämtar eller ställer in sidorna som ska renderas. Standard är alla sidor i dokumentet. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | Hämtar eller ställer in ett värde som avgör om transparenta bilder ska förblandas med svart bakgrundsfärg. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | Anger om Microsoft Word-formulärfält ska bevaras som formulärfält i PDF eller konverteras till text. Standard är`falsk` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | När`sann` , pretty formats output där det är tillämpligt. Standardvärdet är`falsk` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Anropas när ett dokument sparas och accepterar data om sparningsförloppet. |
| [RenderChoiceFormFieldBorder](../../aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/) { get; set; } | Anger om PDF-valformulärets fältkant ska renderas. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | Anger formatet som dokumentet sparas i om detta objekt för sparade alternativ används. Kan endast varaPdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Anger mappen för temporära filer som används när man sparar till en DOC- eller DOCX-fil. Som standard är den här egenskapen`null` och inga temporära filer används. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | Anger komprimeringstyp som ska användas för allt textinnehåll i dokumentet. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Avgör om teckensnittsattributen ska ändras beroende på den teckenkod som används. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) egenskapen uppdateras innan den sparas. Standardvärdet är`falsk` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Hämtar eller anger ett värde som avgör om fält av vissa typer ska uppdateras innan dokumentet sparas till ett fast sidformat. Standardvärdet för den här egenskapen är`sann` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) egenskapen uppdateras innan den sparas. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Hämtar eller ställer in ett värde som avgör om[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) egenskapen uppdateras innan den sparas. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Hämtar eller ställer in ett värde som avgör om antialiasing ska användas för rendering. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | Hämtar eller anger ett booleskt värde som anger om dokumentet ska sparas med en layout för broschyrutskrift, om det anges via[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | Hämtar eller anger ett värde som avgör om TrueType-teckensnitten Arial, Times New Roman, Courier New och Symbol ska ersättas med kärn-PDF Type 1-teckensnitt. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Hämtar eller ställer in ett värde som avgör om högkvalitativa (dvs. långsamma) renderingsalgoritmer ska användas eller inte. |
| [UseSdtTagAsFormFieldName](../../aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/) { get; set; } | Anger om SDT-kontrollens tagg eller Id-egenskap ska användas som namn på formulärfältet i PDF. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior/) { get; set; } | Hämtar eller ställer in ett värde som avgör vilken typ av zoom som ska tillämpas när ett dokument öppnas med en PDF-läsare. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor/) { get; set; } | Hämtar eller ställer in ett värde som bestämmer zoomfaktorn (i procent) för ett dokument. |

## Metoder

| namn | Beskrivning |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone/)() | Skapar en djup klon av detta objekt. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Avgör om det angivna objektet har samma värde som det aktuella objektet. |

## Exempel

Visar hur man ändrar bildfärg med egenskapen för att spara alternativ.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
// Ställ in egenskapen "ColorMode" till "Grayscale" för att rendera alla bilder från dokumentet i svartvitt.
// Storleken på utdatadokumentet kan vara större med den här inställningen.
// Ställ in egenskapen "ColorMode" till "Normal" för att rendera alla bilder i färg.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

Visar hur man tillämpar textkomprimering när man sparar ett dokument till PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Ställ in egenskapen "TextCompression" till "PdfTextCompression.None" för att inte tillämpa några
// komprimering till text när vi sparar dokumentet som PDF.
// Ställ in egenskapen "TextCompression" till "PdfTextCompression.Flate" för att tillämpa ZIP-komprimering
// till text när vi sparar dokumentet som PDF. Ju större dokumentet är, desto större effekt får detta.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Visar hur man konverterar ett helt dokument till PDF med tre nivåer i dokumentdispositionen.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Infoga rubriker för nivå 1 till 5.
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

// Skapa ett "PdfSaveOptions"-objekt som vi kan skicka till dokumentets "Save"-metod
// för att ändra hur den metoden konverterar dokumentet till .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Det utgående PDF-dokumentet kommer att innehålla en disposition, vilket är en innehållsförteckning som listar rubriker i dokumentets brödtext.
// Om du klickar på en post i den här dispositionen kommer vi till platsen för respektive rubrik.
// Sätt egenskapen "HeadingsOutlineLevels" till "4" för att exkludera alla rubriker vars nivåer är över 4 från dispositionen.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Om en dispositionspost har efterföljande poster på en högre nivå mellan sig själv och nästa post på samma eller lägre nivå,
// en pil visas till vänster om posten. Denna post är "ägare" till flera sådana "underposter".
// I vårt dokument är dispositionsposterna från den 5:e rubriknivån underposter till den andra dispositionsposten på den 4:e nivån,
// posterna på rubriknivå 4 och 5 är underposter till den andra posten på nivå 3, och så vidare.
// I dispositionen kan vi klicka på pilen för posten "ägare" för att minimera/expandera alla dess underposter.
// Sätt egenskapen "ExpandedOutlineLevels" till "2" för att automatiskt expandera alla rubriknivå 2 och lägre dispositionsposter
// och komprimerar alla poster på nivå 3 och högre när vi öppnar dokumentet.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Se även

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* namnutrymme [Aspose.Words.Saving](../../aspose.words.saving/)
* hopsättning [Aspose.Words](../../)
