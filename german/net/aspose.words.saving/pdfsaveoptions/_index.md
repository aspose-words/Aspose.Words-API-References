---
title: PdfSaveOptions Class
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.PdfSaveOptions, um Ihr Dokumentspeichererlebnis zu verbessern. Passen Sie die Einstellungen für optimale PDF-Ausgabequalität und -Leistung an.
type: docs
weight: 6320
url: /de/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments imPdf format.

Um mehr zu erfahren, besuchen Sie die[Speicheroptionen festlegen](https://docs.aspose.com/words/net/specify-save-options/) Dokumentationsartikel.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments im verwendet werden kann.Pdf format. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | Ein Flag, das angibt, ob zusätzliche Textpositionierungsoperatoren geschrieben werden sollen oder nicht. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Konturen beim Einbetten von TrueType-Schriftarten in ein Dokument beim Speichern zulässig ist. Der Standardwert ist`FALSCH` . |
| [AttachmentsEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie Anhänge in das PDF-Dokument eingebettet werden. |
| [CacheBackgroundGraphics](../../aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob im Hintergrund des Dokuments platzierte Grafiken zwischengespeichert werden sollen oder nicht. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie Farben gerendert werden. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | Gibt den Konformitätsgrad mit PDF-Standards für Ausgabedokumente an. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | Gibt an, ob Fußnoten-/Endnotenverweise im Haupttext in aktive Hyperlinks umgewandelt werden sollen. Beim Anklicken führt der Hyperlink zur entsprechenden Fußnote/Endnote. Standard ist`FALSCH` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der die Art und Weise bestimmt,[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) werden in eine PDF-Datei exportiert. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ruft die benutzerdefinierte lokale Zeitzone ab, die für Datums-/Uhrzeitfelder verwendet wird, oder legt diese fest. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ruft den Pfad zur Standardvorlage ab oder legt ihn fest (einschließlich Dateiname). Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | Ruft die Details zum Signieren des PDF-Ausgabedokuments ab oder legt sie fest. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | Ein Flag, das angibt, ob in der Titelleiste des Fensters der Dokumenttitel angezeigt werden soll, der dem Titeleintrag des Dokumentinformationswörterbuchs entnommen wurde. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | Ermöglicht die Angabe von Downsampling-Optionen. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | Steuert, wie Schriftarten in die resultierenden PDF-Dokumente eingebettet werden. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | Ruft die Details zum Verschlüsseln des PDF-Ausgabedokuments ab oder legt sie fest. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die Dokumentstruktur exportiert werden soll oder nicht. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Wann`WAHR` , bewirkt, dass der Name und die Version von Aspose.Words in die erstellten Dateien eingebettet werden. Der Standardwert ist`WAHR` . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob zum Exportieren der Textsprache ein „Span“-Tag in der Dokumentstruktur erstellt werden soll oder nicht. |
| [ExportParagraphGraphicsToArtifact](../../aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob eine Absatzgrafik als Artefakt markiert werden soll. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | Gibt den Schriftarteinbettungsmodus an. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | Bestimmt, wie Lesezeichen in Kopf-/Fußzeilen exportiert werden. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | Gibt an, wie der Farbraum für die Bilder im PDF-Dokument ausgewählt wird. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | Gibt den Komprimierungstyp an, der für alle Bilder im Dokument verwendet werden soll. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie InkML-Objekte gerendert werden. |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | Ein Flag, das angibt, ob die Bildinterpolation von einem konformen Reader durchgeführt werden soll. Wenn`FALSCH` angegeben ist, wird das Flag nicht in das Ausgabedokument geschrieben und stattdessen wird das Standardverhalten des Readers verwendet. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der die Qualität der JPEG-Bilder im PDF-Dokument bestimmt. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Ermöglicht die Angabe von Optionen für das Rendern von Metadateien. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Ruft ab oder legt fest[`NumeralFormat`](../numeralformat/) Wird zur Darstellung von Ziffern verwendet. Standardmäßig werden europäische Ziffern verwendet. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Hyperlinks im PDF-Ausgabedokument in einem neuen Fenster (oder Tab) eines Browsers geöffnet werden müssen. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Flag gibt an, ob es zur Optimierung der Ausgabe erforderlich ist. Wenn dieses Flag gesetzt ist, werden redundante verschachtelte Leinwände und leere Leinwände entfernt, auch benachbarte Glyphen mit der gleichen Formatierung werden verkettet. Hinweis: Die Genauigkeit der Inhaltsanzeige kann beeinträchtigt werden, wenn diese Eigenschaft auf`WAHR` . Standard ist`FALSCH` . |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | Ermöglicht die Angabe von Gliederungsoptionen. |
| [PageLayout](../../aspose.words.saving/pdfsaveoptions/pagelayout/) { get; set; } | Gibt das Seitenlayout an, das verwendet werden soll, wenn das Dokument in einem PDF-Reader geöffnet wird. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | Gibt an, wie das PDF-Dokument angezeigt werden soll, wenn es in einem PDF-Reader geöffnet wird. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie einzelne Seiten gespeichert werden, wenn ein Dokument in ein festes Seitenformat exportiert wird. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Ruft die zu rendernden Seiten ab oder legt sie fest. Standardmäßig sind alle Seiten im Dokument dargestellt. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob transparente Bilder mit schwarzer Hintergrundfarbe vorgemischt werden sollen oder nicht. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | Gibt an, ob Microsoft Word-Formularfelder als Formularfelder in PDF erhalten bleiben oder in Text konvertiert werden sollen. Der Standardwert ist`FALSCH` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Wann`WAHR` , formatiert die Ausgabe, wo anwendbar. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten zum Speicherfortschritt. |
| [RenderChoiceFormFieldBorder](../../aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/) { get; set; } | Gibt an, ob der Feldrand des PDF-Auswahlformulars gerendert werden soll. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann nurPdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Gibt den Ordner für temporäre Dateien an, der beim Speichern in eine DOC- oder DOCX-Datei verwendet wird. Standardmäßig ist diese Eigenschaft`null` und es werden keine temporären Dateien verwendet. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | Gibt den Komprimierungstyp an, der für den gesamten Textinhalt im Dokument verwendet werden soll. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Bestimmt, ob die Schriftattribute entsprechend dem verwendeten Zeichencode geändert werden. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) Eigenschaft wird vor dem Speichern aktualisiert. Der Standardwert ist`FALSCH` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Anti-Aliasing zum Rendern verwendet werden soll oder nicht. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Dokument im Broschüren-Drucklayout gespeichert werden soll, wenn dies über[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob die TrueType-Schriftarten Arial, Times New Roman, Courier New und Symbol durch PDF Type 1-Kernschriftarten ersetzt werden sollen oder nicht. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob qualitativ hochwertige (d. h. langsame) Rendering-Algorithmen verwendet werden sollen oder nicht. |
| [UseSdtTagAsFormFieldName](../../aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/) { get; set; } | Gibt an, ob das SDT-Steuerelement-Tag oder die ID-Eigenschaft als Name des Formularfelds in PDF verwendet werden soll. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, welche Art von Zoom angewendet werden soll, wenn ein Dokument mit einem PDF-Viewer geöffnet wird. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der den Zoomfaktor (in Prozent) für ein Dokument bestimmt. |

## Methoden

| Name | Beschreibung |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone/)() | Erstellt einen tiefen Klon dieses Objekts. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Bestimmt, ob das angegebene Objekt den gleichen Wert wie das aktuelle Objekt hat. |

## Beispiele

Zeigt, wie die Bildfarbe mit der Eigenschaft „Speicheroptionen“ geändert wird.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
// Setzen Sie die Eigenschaft „ColorMode“ auf „Graustufen“, um alle Bilder aus dem Dokument in Schwarzweiß darzustellen.
// Die Größe des Ausgabedokuments kann mit dieser Einstellung größer sein.
// Setzen Sie die Eigenschaft „ColorMode“ auf „Normal“, um alle Bilder in Farbe darzustellen.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

Zeigt, wie beim Speichern eines Dokuments im PDF-Format eine Textkomprimierung angewendet wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Setzen Sie die Eigenschaft „TextCompression“ auf „PdfTextCompression.None“, um keine
// Komprimierung auf Text, wenn wir das Dokument als PDF speichern.
// Setzen Sie die Eigenschaft „TextCompression“ auf „PdfTextCompression.Flate“, um die ZIP-Komprimierung anzuwenden
// in Text, wenn wir das Dokument als PDF speichern. Je größer das Dokument, desto größer sind die Auswirkungen.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Zeigt, wie ein ganzes Dokument mit drei Ebenen in der Dokumentgliederung in PDF konvertiert wird.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Überschriften der Ebenen 1 bis 5 einfügen.
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

// Erstellen Sie ein "PdfSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
// um zu ändern, wie diese Methode das Dokument in .PDF konvertiert.
PdfSaveOptions options = new PdfSaveOptions();

// Das ausgegebene PDF-Dokument enthält eine Gliederung, d. h. ein Inhaltsverzeichnis, das die Überschriften im Dokumenttext auflistet.
// Durch Klicken auf einen Eintrag in dieser Gliederung gelangen wir zur Position der entsprechenden Überschrift.
// Setzen Sie die Eigenschaft „HeadingsOutlineLevels“ auf „4“, um alle Überschriften, deren Ebenen über 4 liegen, aus der Gliederung auszuschließen.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Wenn ein Gliederungseintrag nachfolgende Einträge einer höheren Ebene zwischen sich selbst und dem nächsten Eintrag der gleichen oder niedrigeren Ebene hat,
// links neben dem Eintrag erscheint ein Pfeil. Dieser Eintrag ist der „Eigentümer“ mehrerer solcher „Untereinträge“.
// In unserem Dokument sind die Gliederungseinträge der 5. Überschriftenebene Untereinträge des zweiten Gliederungseintrags der 4. Ebene,
// Die Einträge der 4. und 5. Überschriftenebene sind Untereinträge des zweiten Eintrags der 3. Ebene und so weiter.
// In der Gliederung können wir auf den Pfeil des Eintrags „Eigentümer“ klicken, um alle Untereinträge auszublenden/einzuklappen.
// Setzen Sie die Eigenschaft „ExpandedOutlineLevels“ auf „2“, um alle Gliederungseinträge der Überschriftenebene 2 und darunter automatisch zu erweitern
// und reduzieren Sie alle Einträge der Ebene 3 und höher, wenn wir das Dokument öffnen.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Siehe auch

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
