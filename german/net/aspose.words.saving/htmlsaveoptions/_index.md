---
title: Class HtmlSaveOptions
second_title: Aspose.Words für .NET-API-Referenz
description: Aspose.Words.Saving.HtmlSaveOptions klas. Kann verwendet werden um zusätzliche Optionen beim Speichern eines Dokuments im zu spezifizierenHtml  Mhtml oderEpub format.
type: docs
weight: 4850
url: /de/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Kann verwendet werden, um zusätzliche Optionen beim Speichern eines Dokuments im zu spezifizierenHtml , Mhtml oderEpub format.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Konstrukteure

| Name | Beschreibung |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument in der zu speichernHtml format. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(SaveFormat) | Initialisiert eine neue Instanz dieser Klasse, die verwendet werden kann, um ein Dokument in der zu speichernHtml ,Mhtml oderEpub format. |

## Eigenschaften

| Name | Beschreibung |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ruft einen booleschen Wert ab oder legt ihn fest, der angibt, ob das Einbetten von Schriftarten mit PostScript-Konturen zulässig ist, wenn TrueType-Schriftarten in ein Dokument eingebettet werden, nachdem es gespeichert wurde. Der Standardwert ist **FALSCH** . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | Gibt an, ob negative linke und rechte Einzüge von Absätzen beim Speichern in HTML, MHTML oder EPUB normalisiert werden. Standardwert ist`FALSCH` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | Gibt ein Präfix an, das allen CSS-Klassennamen hinzugefügt wird. Der Standardwert ist eine leere Zeichenfolge, und generierte CSS-Klassennamen haben kein gemeinsames Präfix. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie CSS-Stile gespeichert werden, wenn ein Dokument in HTML, MHTML oder EPUB gespeichert wird. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | Gibt den Pfad und den Namen der CSS-Datei (Cascading Style Sheet) an, die geschrieben wird, wenn ein Dokument in HTML exportiert wird. Standard ist eine leere Zeichenfolge. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | Gibt an, wie CSS-Stile (Cascading Style Sheet) nach HTML, MHTML oder EPUB exportiert werden. Der Standardwert istInline für HTML/MHTML und External für EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ruft eine benutzerdefinierte lokale Zeitzone ab oder legt sie fest, die für Datums-/Uhrzeitfelder verwendet wird. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ruft den Pfad zur Standardvorlage (einschließlich Dateiname) ab oder legt ihn fest. Der Standardwert für diese Eigenschaft ist **leerer String** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie 3D-Effekte gerendert werden. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie DrawingML-Effekte gerendert werden. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, wie DrawingML-Formen gerendert werden. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie Dokumentteile gespeichert werden, wenn ein Dokument in HTML oder EPUB gespeichert wird. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | Gibt an, wie das Dokument beim Speichern aufgeteilt werden sollHtml oderEpub Format. Standard istNone für HTML und HeadingParagraph für EPUB. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | Gibt die maximale Überschriftenebene an, bei der das Dokument geteilt werden soll. Der Standardwert ist`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | Gibt die beim Exportieren in HTML, MHTML oder EPUB zu verwendende Kodierung an. Der Standardwert ist`neue UTF8-Kodierung (false)` (UTF-8 ohne BOM). |
| [EpubNavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/epubnavigationmaplevel/) { get; set; } | Gibt die maximale Ebene von Überschriften an, die beim Exportieren in das IDPF-EPUB-Format in die Navigationskarte eingetragen werden. Der Standardwert ist`3` . |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | Gibt an, ob CID-URLs (Content-ID) verwendet werden sollen, um auf Ressourcen (Bilder, Schriftarten, CSS) zu verweisen, die in MHTML -Dokumenten enthalten sind. Standardwert ist`FALSCH` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | Gibt an, ob integrierte und benutzerdefinierte Dokumenteigenschaften nach HTML, MHTML oder EPUB exportiert werden. Der Standardwert ist`FALSCH` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | Steuert, wie Dropdown-Formularfelder in HTML oder MHTML gespeichert werden. Standardwert ist`FALSCH` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | Gibt an, ob Schriftressourcen in HTML, MHTML oder EPUB exportiert werden sollen. Standard ist`FALSCH` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | Gibt an, ob Schriftartressourcen in HTML in Base64-Codierung eingebettet werden sollen. Standard ist`FALSCH` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Wenn wahr, bewirkt dies, dass der Name und die Version von Aspose.Words in produzierte Dateien eingebettet werden. Der Standardwert ist **Stimmt** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | Legt fest, wie Kopf- und Fußzeilen in HTML, MHTML oder EPUB ausgegeben werden. Standardwert istPerSection für HTML/MHTML undNone für EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | Gibt an, ob Bilder im Base64-Format zur Ausgabe in HTML, MHTML oder EPUB gespeichert werden. Standard ist`FALSCH` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | Gibt an, ob Sprachinformationen in HTML, MHTML oder EPUB exportiert werden. Standard ist`FALSCH` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | Steuert, wie Listenbezeichnungen in HTML, MHTML oder EPUB ausgegeben werden. Standardwert istAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | Gibt an, ob die Original-URL als URL der verlinkten Bilder verwendet werden soll. Standardwert ist`FALSCH` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | Gibt an, ob Seitenränder in HTML, MHTML oder EPUB exportiert werden. Standard ist`FALSCH` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | Gibt an, ob die Seiteneinrichtung in HTML, MHTML oder EPUB exportiert wird. Standard ist`FALSCH` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | Gibt an, ob Schriftgrößen beim Speichern in HTML, MHTML oder EPUB in relativen Einheiten ausgegeben werden sollen. Standard ist`FALSCH` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | Gibt an, ob die Roundtrip-Informationen beim Speichern in HTML, MHTML oder EPUB geschrieben werden. Der Standardwert ist`Stimmt` für HTML u`FALSCH` für MHTML und EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | Steuert ob[`Shape`](../../aspose.words.drawing/shape/) Knoten werden beim Speichern in HTML, MHTML oder EPUB in SVG-Bilder konvertiert. Standardwert ist`FALSCH` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | Steuert, wie Texteingabeformularfelder in HTML oder MHTML gespeichert werden. Standardwert ist`FALSCH` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | Gibt an, ob beim Speichern von HTML, MHTML und EPUB Seitenzahlen in das Inhaltsverzeichnis geschrieben werden sollen. Der Standardwert ist`FALSCH` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | Gibt an, ob die DOCTYPE-Deklaration beim Speichern in HTML oder MHTML geschrieben werden soll. Wann`Stimmt` , schreibt eine DOCTYPE-Deklaration in das Dokument vor dem Wurzelelement. Standardwert ist`FALSCH`. Beim Speichern in EPUB oder HTML5 (Html5 ) wird immer die Deklaration DOCTYPE geschrieben. |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Erhält oder setzt einen Wert, der festlegt, welche Dokumentformate abgebildet werden dürfen[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Nur standardmäßigFlatOpc Dokumentformat darf gemappt werden. |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | Steuert, welche Font-Ressourcen beim Speichern in HTML, MHTML oder EPUB unterteilt werden müssen. Standard ist`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie Schriftarten gespeichert werden, wenn ein Dokument in HTML, MHTML oder EPUB gespeichert wird. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | Gibt den physischen Ordner an, in dem Schriftarten gespeichert werden, wenn ein Dokument in HTML exportiert wird. Standard ist eine leere Zeichenfolge. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | Gibt den Namen des Ordners an, der zum Erstellen von Schriftart-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Standard ist eine leere Zeichenfolge. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | Gibt die Version des HTML-Standards an, die verwendet werden soll, wenn das Dokument in HTML oder MHTML gespeichert wird. Der Standardwert istXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | Gibt die Ausgabeauflösung für Bilder beim Exportieren in HTML, MHTML oder EPUB an. Standard ist`96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | Ermöglicht die Steuerung, wie Bilder gespeichert werden, wenn ein Dokument in HTML, MHTML oder EPUB gespeichert wird. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | Gibt den physischen Ordner an, in dem Bilder gespeichert werden, wenn ein Dokument in das HTML-Format exportiert wird. Standard ist eine leere Zeichenfolge. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | Gibt den Namen des Ordners an, der zum Erstellen von Bild-URIs verwendet wird, die in ein HTML-Dokument geschrieben werden. Standard ist eine leere Zeichenfolge. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ruft einen Wert ab oder legt einen Wert fest, der bestimmt, wie Ink-Objekte (InkML) gerendert werden. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Holt oder legt einen Wert fest, der bestimmt, ob eine Speicheroptimierung durchgeführt werden soll, bevor das Dokument gespeichert wird. Der Standardwert für diese Eigenschaft ist **FALSCH** . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | Gibt an, in welchem Format Metadateien gespeichert werden, wenn sie in HTML, MHTML oder EPUB exportiert werden. Standardwert istPng , was bedeutet, dass Metadateien in Raster-PNG-Bilder gerendert werden. |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | Steuert, wie OfficeMath-Objekte in HTML, MHTML oder EPUB exportiert werden. Standardwert ist`HtmlOfficeMathOutputMode.Image` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Wann`Stimmt` , gibt gegebenenfalls hübsche Formate aus. Standardwert ist **FALSCH** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Wird beim Speichern eines Dokuments aufgerufen und akzeptiert Daten zum Speicherfortschritt. |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | Gibt an, ob im Dokument verwendete Schriftfamiliennamen aufgelöst und gemäß ersetzt werden[`FontSettings`](../../aspose.words/document/fontsettings/) beim Schreiben in HTML-basierte Formate. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | Gibt einen physischen Ordner an, in dem alle Ressourcen wie Bilder, Schriftarten und externes CSS gespeichert werden, wenn ein document in HTML exportiert wird. Standard ist eine leere Zeichenfolge. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | Gibt den Namen des Ordners an, der verwendet wird, um URIs aller Ressourcen zu erstellen, die in ein HTML-Dokument geschrieben werden. Standard ist eine leere Zeichenfolge. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | Gibt das Format an, in dem das Dokument gespeichert wird, wenn dieses Speicheroptionsobjekt verwendet wird. Kann seinHtml ,Mhtml oderEpub . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | Gibt an, ob Bilder beim Exportieren nach HTML, MHTML oder EPUB von Aspose.Words auf die Größe der Begrenzungsform skaliert werden. Standardwert ist`Stimmt` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | Steuert, wie Tabellen-, Zeilen- und Zellenbreiten nach HTML, MHTML oder EPUB exportiert werden. Standardwert istAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Gibt den Ordner für temporäre Dateien an, der beim Speichern in eine DOC- oder DOCX-Datei verwendet wird. Standardmäßig ist diese Eigenschaft`Null` und es werden keine temporären Dateien verwendet. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) Eigenschaft wird vor dem Speichern aktualisiert. Standardwert ist false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Felder bestimmter Typen aktualisiert werden sollen, bevor das Dokument in einem festen Seitenformat gespeichert wird. Der Standardwert für diese Eigenschaft ist **Stimmt** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob die[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) Eigenschaft wird vor dem Speichern aktualisiert. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Erhält oder setzt den Wert, der bestimmt, ob der Inhalt von[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) wird vor dem Speichern aktualisiert. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob Anti-Aliasing für das Rendern verwendet werden soll oder nicht. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ruft einen Wert ab oder legt ihn fest, der bestimmt, ob qualitativ hochwertige (dh langsame) Renderalgorithmen verwendet werden sollen oder nicht. |

### Beispiele

Zeigt, wie der Ordner zum Speichern verknüpfter Bilder nach dem Speichern in .html angegeben wird.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Legen Sie eine Option zum Exportieren von Formularfeldern als einfachen Text anstelle von HTML-Eingabeelementen fest.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Zeigt, wie Sie beim Speichern eines Dokuments im .epub-Format eine bestimmte Codierung verwenden.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Verwenden Sie ein SaveOptions-Objekt, um die Kodierung für ein zu speicherndes Dokument anzugeben.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Standardmäßig hat ein ausgegebenes .epub-Dokument seinen gesamten Inhalt in einem HTML-Teil.
// Ein Split-Kriterium ermöglicht es uns, das Dokument in mehrere HTML-Teile zu segmentieren.
// Wir werden die Kriterien festlegen, um das Dokument in Überschriftenabsätze aufzuteilen.
// Dies ist nützlich für Leser, die keine HTML-Dateien lesen können, die größer als eine bestimmte Größe sind.
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

    // Wenn wir das Dokument normal speichern, gibt es eine HTML-Ausgabe
    // Dokument mit dem gesamten Inhalt des Quelldokuments.
    // Legen Sie die Eigenschaft „DocumentSplitCriteria“ auf „DocumentSplitCriteria.SectionBreak“ fest
    // Unser Dokument in mehreren HTML-Dateien speichern: eine für jeden Abschnitt.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Weisen Sie der Eigenschaft "DocumentPartSavingCallback" einen benutzerdefinierten Rückruf zu, um die Speicherlogik des Dokumentteils zu ändern.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Wenn wir ein Dokument, das Bilder enthält, in HTML umwandeln, erhalten wir am Ende eine HTML-Datei, die auf mehrere Bilder verweist.
    // Jedes Bild liegt in Form einer Datei im lokalen Dateisystem vor.
    // Es gibt auch einen Rückruf, der den Namen und den Speicherort des Dateisystems jedes Bildes anpassen kann.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Legt benutzerdefinierte Dateinamen für Ausgabedokumente fest, in die der Speichervorgang ein Dokument aufteilt.
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
        // Über die Eigenschaft "Document" können wir auf das gesamte Quelldokument zugreifen.
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

        // Im Folgenden finden Sie zwei Möglichkeiten, um anzugeben, wo Aspose.Words jeden Teil des Dokuments speichern wird.
        // 1 - Legen Sie einen Dateinamen für die Ausgabeteildatei fest:
        args.DocumentPartFileName = partFileName;

        // 2 - Erstellen Sie einen benutzerdefinierten Stream für die Ausgabeteildatei:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Legt benutzerdefinierte Dateinamen für Bilddateien fest, die eine HTML-Konvertierung erstellt.
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

        // Im Folgenden finden Sie zwei Möglichkeiten, um anzugeben, wo Aspose.Words jeden Teil des Dokuments speichern wird.
        // 1 - Legen Sie einen Dateinamen für die Ausgabebilddatei fest:
        args.ImageFileName = imageFileName;

        // 2 - Erstellen Sie einen benutzerdefinierten Stream für die Ausgabebilddatei:
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


