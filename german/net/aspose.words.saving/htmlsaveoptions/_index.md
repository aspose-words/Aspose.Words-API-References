---
title: HtmlSaveOptions Class
linktitle: HtmlSaveOptions
articleTitle: HtmlSaveOptions
second_title: Aspose.Words für .NET
description: Entdecken Sie Aspose.Words.Saving.HtmlSaveOptions, um das Speichern von Dokumenten in den Formaten HTML, MHTML, EPUB, AZW3 und MOBI mit anpassbaren Optionen zu verbessern.
type: docs
weight: 5860
url: /de/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im anzugebenHtml ,Mhtml ,Epub , Azw3 oderMobi format.

Um mehr zu erfahren, besuchen Sie die[Speicheroptionen festlegen](https://docs.aspose.com/words/net/specify-save-options/) Dokumentationsartikel.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments imHtml format. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Initialisiert eine neue Instanz dieser Klasse, die zum Speichern eines Dokuments imHtml ,Mhtml ,Epub , Azw3 oderMobi format. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Konturen beim Einbetten von TrueType-Schriftarten in ein Dokument beim Speichern zulässig ist. Der Standardwert ist`FALSCH` . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | Gibt an, ob negative linke und rechte Einzüge von Absätzen beim Speichern in HTML, MHTML oder EPUB normalisiert werden. Der Standardwert ist`FALSCH` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | Gibt ein Präfix an, das allen CSS-Klassennamen hinzugefügt wird. Der Standardwert ist eine leere Zeichenfolge und generierte CSS-Klassennamen haben kein gemeinsames Präfix. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie CSS-Stile gespeichert werden, wenn ein Dokument im HTML-, MHTML- oder EPUB-Format gespeichert wird. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | Gibt den Pfad und den Namen der Cascading Style Sheet (CSS)-Datei an, die geschrieben wird, wenn ein Dokument nach HTML exportiert wird. Der Standardwert ist eine leere Zeichenfolge. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | Gibt an, wie CSS-Stile (Cascading Style Sheet) in HTML, MHTML oder EPUB exportiert werden. Der Standardwert istInline für HTML/MHTML und External für EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ruft die benutzerdefinierte lokale Zeitzone ab, die für Datums-/Uhrzeitfelder verwendet wird, oder legt diese fest. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ruft den Pfad zur Standardvorlage ab oder legt ihn fest (einschließlich Dateiname). Der Standardwert für diese Eigenschaft ist**leere Zeichenfolge** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie Dokumentteile gespeichert werden, wenn ein Dokument im HTML- oder EPUB-Format gespeichert wird. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | Gibt an, wie das Dokument beim Speichern aufgeteilt werden soll.Html , Epub oderAzw3 format. Standard istNone für HTML und HeadingParagraph für EPUB und AZW3. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | Gibt die maximale Überschriftenebene an, bei der das Dokument aufgeteilt werden soll. Der Standardwert ist`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | Gibt die Kodierung an, die beim Exportieren in HTML, MHTML oder EPUB verwendet werden soll. Der Standardwert ist`neue UTF8-Kodierung (falsch)` (UTF-8 ohne BOM). |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | Gibt an, ob CID-URLs (Content-ID) zum Verweisen auf Ressourcen (Bilder, Schriftarten, CSS) in MHTML -Dokumenten verwendet werden sollen. Der Standardwert ist`FALSCH` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | Gibt an, ob integrierte und benutzerdefinierte Dokumenteigenschaften in HTML, MHTML oder EPUB exportiert werden sollen. Der Standardwert ist`FALSCH` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | Steuert, wie Dropdown-Formularfelder in HTML oder MHTML gespeichert werden. Der Standardwert ist`FALSCH` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | Gibt an, ob Schriftressourcen in HTML, MHTML oder EPUB exportiert werden sollen. Standard ist`FALSCH` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | Gibt an, ob Schriftartenressourcen in Base64-Kodierung in HTML eingebettet werden sollen. Standard ist`FALSCH` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Wann`WAHR` , bewirkt, dass der Name und die Version von Aspose.Words in die erstellten Dateien eingebettet werden. Der Standardwert ist`WAHR` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | Gibt an, wie Kopf- und Fußzeilen in HTML, MHTML oder EPUB ausgegeben werden. Der Standardwert istPerSection für HTML/MHTML undNone für EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | Gibt an, ob Bilder im Base64-Format in den Ausgabeformaten HTML, MHTML oder EPUB gespeichert werden. Standard ist`FALSCH` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | Gibt an, ob Sprachinformationen in HTML, MHTML oder EPUB exportiert werden. Standard ist`FALSCH` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | Steuert, wie Listenbeschriftungen in HTML, MHTML oder EPUB ausgegeben werden. Der Standardwert istAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | Gibt an, ob die ursprüngliche URL als URL der verknüpften Bilder verwendet werden soll. Der Standardwert ist`FALSCH` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | Gibt an, ob Seitenränder in HTML, MHTML oder EPUB exportiert werden. Standard ist`FALSCH` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | Gibt an, ob die Seiteneinrichtung in HTML, MHTML oder EPUB exportiert wird. Standard ist`FALSCH` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | Gibt an, ob Schriftgrößen beim Speichern in HTML, MHTML oder EPUB in relativen Einheiten ausgegeben werden sollen. Standard ist`FALSCH` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | Gibt an, ob die Roundtrip-Informationen beim Speichern in HTML, MHTML oder EPUB geschrieben werden sollen. Der Standardwert ist`WAHR` für HTML und`FALSCH` für MHTML und EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | Steuert, ob[`Shape`](../../aspose.words.drawing/shape/)Knoten werden beim Speichern in HTML, MHTML, EPUB oder AZW3 in SVG-Bilder konvertiert. Der Standardwert ist`FALSCH` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | Steuert, wie Texteingabeformularfelder in HTML oder MHTML gespeichert werden. Der Standardwert ist`FALSCH` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | Gibt an, ob beim Speichern von HTML, MHTML und EPUB Seitenzahlen in das Inhaltsverzeichnis geschrieben werden sollen. Der Standardwert ist`FALSCH` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | Gibt an, ob die DOCTYPE-Deklaration beim Speichern in HTML oder MHTML geschrieben werden soll. Wenn`WAHR` , schreibt eine DOCTYPE-Deklaration in das Dokument vor dem Stammelement. Der Standardwert ist`FALSCH`. Beim Speichern im EPUB- oder HTML5-Format (Html5 ) wird immer die DOCTYPE -Deklaration geschrieben. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | Steuert, welche Schriftartressourcen beim Speichern in HTML, MHTML oder EPUB untergeordnet werden müssen. Standard ist`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie Schriftarten gespeichert werden, wenn ein Dokument im HTML-, MHTML- oder EPUB-Format gespeichert wird. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | Gibt den physischen Ordner an, in dem Schriftarten beim Exportieren eines Dokuments nach HTML gespeichert werden. Der Standardwert ist eine leere Zeichenfolge. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | Gibt den Namen des Ordners an, der zum Erstellen von Schriftart-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Der Standardwert ist eine leere Zeichenfolge. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | Gibt die Version des HTML-Standards an, die beim Speichern des Dokuments im HTML- oder MHTML-Format verwendet werden soll. Der Standardwert istXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | Gibt die Ausgabeauflösung für Bilder beim Exportieren in HTML, MHTML oder EPUB an. Standard ist`96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie Bilder gespeichert werden, wenn ein Dokument im HTML-, MHTML- oder EPUB-Format gespeichert wird. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | Gibt den physischen Ordner an, in dem Bilder beim Exportieren eines Dokuments in das HTML-Format gespeichert werden. Der Standardwert ist eine leere Zeichenfolge. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Der Standardwert ist eine leere Zeichenfolge. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie InkML-Objekte gerendert werden. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob vor dem Speichern des Dokuments eine Speicheroptimierung durchgeführt werden soll. Der Standardwert für diese Eigenschaft ist`FALSCH` . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | Gibt an, in welchem Format Metadateien beim Exportieren in HTML, MHTML oder EPUB gespeichert werden. Der Standardwert istPng , was bedeutet, dass Metadateien in Raster-PNG-Bilder gerendert werden. |
| [NavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/navigationmaplevel/) { get; set; } | Gibt die maximale Überschriftenebene an, die beim Export in die Formate EPUB, MOBI oder AZW3 in die Navigationskarte eingefügt wird. Der Standardwert ist`3` . |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | Steuert, wie OfficeMath-Objekte in HTML, MHTML oder EPUB exportiert werden. Der Standardwert istImage . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Wann`WAHR` , formatiert die Ausgabe, wo anwendbar. Der Standardwert ist`FALSCH` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten zum Speicherfortschritt. |
| [RemoveJavaScriptFromLinks](../../aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/) { get; set; } | Gibt an, ob JavaScript aus Links entfernt wird. Standard ist`FALSCH` . |
| [ReplaceBackslashWithYenSign](../../aspose.words.saving/htmlsaveoptions/replacebackslashwithyensign/) { get; set; } | Gibt an, ob Backslash-Zeichen durch Yen-Zeichen ersetzt werden sollen. Der Standardwert ist`FALSCH` . |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | Gibt an, ob die im Dokument verwendeten Schriftfamiliennamen aufgelöst und ersetzt werden gemäß [`FontSettings`](../../aspose.words/document/fontsettings/) beim Schreiben in HTML-basierte Formate. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | Gibt einen physischen Ordner an, in dem alle Ressourcen wie Bilder, Schriftarten und externes CSS gespeichert werden, wenn ein Dokument nach HTML exportiert wird. Der Standardwert ist eine leere Zeichenfolge. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | Gibt den Namen des Ordners an, der zum Erstellen der URIs aller in ein HTML-Dokument geschriebenen Ressourcen verwendet wird. Der Standardwert ist eine leere Zeichenfolge. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann seinHtml ,Mhtml ,Epub , Azw3 oderMobi . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | Gibt an, ob Bilder von Aspose.Words beim Exportieren in HTML, MHTML oder EPUB auf die Größe der Begrenzungsform skaliert werden. Der Standardwert ist`WAHR` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | Steuert, wie Tabellen-, Zeilen- und Zellenbreiten in HTML, MHTML oder EPUB exportiert werden. Der Standardwert istAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Gibt den Ordner für temporäre Dateien an, der beim Speichern in eine DOC- oder DOCX-Datei verwendet wird. Standardmäßig ist diese Eigenschaft`null` und es werden keine temporären Dateien verwendet. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Bestimmt, ob die Schriftattribute entsprechend dem verwendeten Zeichencode geändert werden. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) Eigenschaft wird vor dem Speichern aktualisiert. Der Standardwert ist`FALSCH` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist`WAHR` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, ob Anti-Aliasing zum Rendern verwendet werden soll oder nicht. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob qualitativ hochwertige (d. h. langsame) Rendering-Algorithmen verwendet werden sollen oder nicht. |

## Beispiele

Zeigt, wie der Ordner zum Speichern verknüpfter Bilder nach dem Speichern im HTML-Format angegeben wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Legen Sie eine Option fest, um Formularfelder als einfachen Text statt als HTML-Eingabeelemente zu exportieren.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Zeigt, wie beim Speichern eines Dokuments im EPUB-Format eine bestimmte Kodierung verwendet wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Verwenden Sie ein SaveOptions-Objekt, um die Kodierung für ein Dokument anzugeben, das wir speichern möchten.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Standardmäßig enthält ein Ausgabedokument im EPUB-Format seinen gesamten Inhalt in einem HTML-Teil.
// Ein Split-Kriterium ermöglicht es uns, das Dokument in mehrere HTML-Teile zu segmentieren.
// Wir legen die Kriterien fest, um das Dokument in Überschriftenabsätze aufzuteilen.
// Dies ist nützlich für Leser, die keine HTML-Dateien lesen können, die eine bestimmte Größe überschreiten.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Geben Sie an, dass wir Dokumenteigenschaften exportieren möchten.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Zeigt, wie ein Dokument in Teile aufgeteilt und gespeichert wird.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Erstellen Sie ein "HtmlFixedSaveOptions"-Objekt, das wir an die "Save"-Methode des Dokuments übergeben können
    // um zu ändern, wie wir das Dokument in HTML konvertieren.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Wenn wir das Dokument normal speichern, gibt es eine Ausgabe-HTML
    // Dokument mit dem gesamten Inhalt des Quelldokuments.
    // Setzen Sie die Eigenschaft "DocumentSplitCriteria" auf "DocumentSplitCriteria.SectionBreak" auf
    // unser Dokument in mehreren HTML-Dateien speichern: eine für jeden Abschnitt.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Weisen Sie der Eigenschaft „DocumentPartSavingCallback“ einen benutzerdefinierten Rückruf zu, um die Logik zum Speichern von Dokumentteilen zu ändern.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Wenn wir ein Dokument, das Bilder enthält, in HTML konvertieren, erhalten wir am Ende eine HTML-Datei, die auf mehrere Bilder verweist.
    // Jedes Bild liegt in Form einer Datei im lokalen Dateisystem vor.
    // Es gibt auch einen Rückruf, mit dem der Name und der Dateisystemspeicherort jedes Bildes angepasst werden können.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Legt benutzerdefinierte Dateinamen für Ausgabedokumente fest, in die beim Speichern ein Dokument aufgeteilt wird.
/// </summary>
private class SavedDocumentPartRename : IDocumentPartSavingCallback
{
    public SavedDocumentPartRename(string outFileName, DocumentSplitCriteria documentSplitCriteria)
    {
        mOutFileName = outFileName;
        mDocumentSplitCriteria = documentSplitCriteria;
    }

    void IDocumentPartSavingCallback.DocumentPartSaving(DocumentPartSavingArgs args)
    {
        // Über die Eigenschaft „Dokument“ können wir auf das gesamte Quelldokument zugreifen.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        string partType = string.Empty;

        switch (mDocumentSplitCriteria)
        {
            case DocumentSplitCriteria.PageBreak:
                partType = "Page";
                break;
            case DocumentSplitCriteria.ColumnBreak:
                partType = "Column";
                break;
            case DocumentSplitCriteria.SectionBreak:
                partType = "Section";
                break;
            case DocumentSplitCriteria.HeadingParagraph:
                partType = "Paragraph from heading";
                break;
        }

        string partFileName = $"{mOutFileName} part {++mCount}, of type {partType}{Path.GetExtension(args.DocumentPartFileName)}";

        // Unten finden Sie zwei Möglichkeiten, anzugeben, wo Aspose.Words jeden Teil des Dokuments speichern soll.
        // 1 – Legen Sie einen Dateinamen für die Ausgabeteildatei fest:
        args.DocumentPartFileName = partFileName;

        // 2 – Erstellen Sie einen benutzerdefinierten Stream für die Ausgabeteildatei:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Legt benutzerdefinierte Dateinamen für Bilddateien fest, die bei einer HTML-Konvertierung erstellt werden.
/// </summary>
public class SavedImageRename : IImageSavingCallback
{
    public SavedImageRename(string outFileName)
    {
        mOutFileName = outFileName;
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        string imageFileName = $"{mOutFileName} shape {++mCount}, of type {args.CurrentShape.ShapeType}{Path.GetExtension(args.ImageFileName)}";

        // Unten finden Sie zwei Möglichkeiten, anzugeben, wo Aspose.Words jeden Teil des Dokuments speichern soll.
        // 1 – Legen Sie einen Dateinamen für die Ausgabebilddatei fest:
        args.ImageFileName = imageFileName;

        // 2 – Erstellen Sie einen benutzerdefinierten Stream für die Ausgabebilddatei:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Siehe auch

* class [SaveOptions](../saveoptions/)
* namensraum [Aspose.Words.Saving](../../aspose.words.saving/)
* Montage [Aspose.Words](../../)
