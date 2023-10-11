---
title: Class HtmlSaveOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.HtmlSaveOptions classe. Può essere utilizzato per specificare opzioni aggiuntive quando si salva un documento in Html Mhtml Epub  Azw3 OMobi formato.
type: docs
weight: 5110
url: /it/net/aspose.words.saving/htmlsaveoptions/
---
## HtmlSaveOptions class

Può essere utilizzato per specificare opzioni aggiuntive quando si salva un documento in Html ,Mhtml ,Epub , Azw3 OMobi formato.

Per saperne di più, visita il[Specificare le opzioni di salvataggio](https://docs.aspose.com/words/net/specify-save-options/) articolo di documentazione.

```csharp
public class HtmlSaveOptions : SaveOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [HtmlSaveOptions](htmlsaveoptions/#constructor)() | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nellaHtml formato. |
| [HtmlSaveOptions](htmlsaveoptions/#constructor_1)(SaveFormat) | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nellaHtml ,Mhtml ,Epub , Azw3 OMobi formato. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di caratteri con contorni PostScript quando si incorporano caratteri TrueType in un documento al momento del salvataggio. Il valore predefinito è`falso` . |
| [AllowNegativeIndent](../../aspose.words.saving/htmlsaveoptions/allownegativeindent/) { get; set; } | Specifica se i rientri negativi sinistro e destro dei paragrafi vengono normalizzati durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è`falso` . |
| [CssClassNamePrefix](../../aspose.words.saving/htmlsaveoptions/cssclassnameprefix/) { get; set; } | Specifica un prefisso che viene aggiunto a tutti i nomi delle classi CSS. Il valore predefinito è una stringa vuota e i nomi delle classi CSS generati non hanno prefisso comune. |
| [CssSavingCallback](../../aspose.words.saving/htmlsaveoptions/csssavingcallback/) { get; set; } | Permette di controllare come vengono salvati gli stili CSS quando un documento viene salvato in HTML, MHTML o EPUB. |
| [CssStyleSheetFileName](../../aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/) { get; set; } | Specifica il percorso e il nome del file CSS (Cascading Style Sheet) scritto quando un documento viene esportato in HTML. Il valore predefinito è una stringa vuota. |
| [CssStyleSheetType](../../aspose.words.saving/htmlsaveoptions/cssstylesheettype/) { get; set; } | Specifica come gli stili CSS (Cascading Style Sheet) vengono esportati in HTML, MHTML o EPUB. Il valore predefinito èInline per HTML/MHTML e External per EPUB. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **stringa vuota** (Empty). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering delle forme DrawingML. |
| [DocumentPartSavingCallback](../../aspose.words.saving/htmlsaveoptions/documentpartsavingcallback/) { get; set; } | Permette di controllare come vengono salvate le parti del documento quando un documento viene salvato in HTML o EPUB. |
| [DocumentSplitCriteria](../../aspose.words.saving/htmlsaveoptions/documentsplitcriteria/) { get; set; } | Specifica come deve essere diviso il documento durante il salvataggio inHtml , Epub OAzw3 formato. L'impostazione predefinita èNone per HTML e HeadingParagraph per EPUB e AZW3. |
| [DocumentSplitHeadingLevel](../../aspose.words.saving/htmlsaveoptions/documentsplitheadinglevel/) { get; set; } | Specifica il livello massimo di intestazioni a cui dividere il documento. Il valore predefinito è`2` . |
| [Encoding](../../aspose.words.saving/htmlsaveoptions/encoding/) { get; set; } | Specifica la codifica da utilizzare durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è`nuova codifica UTF8(falso)` (UTF-8 senza distinta base). |
| [ExportCidUrlsForMhtmlResources](../../aspose.words.saving/htmlsaveoptions/exportcidurlsformhtmlresources/) { get; set; } | Specifica se utilizzare gli URL CID (Content-ID) per fare riferimento alle risorse (immagini, caratteri, CSS) incluse nei documenti MHTML . Il valore predefinito è`falso` . |
| [ExportDocumentProperties](../../aspose.words.saving/htmlsaveoptions/exportdocumentproperties/) { get; set; } | Specifica se esportare le proprietà del documento integrate e personalizzate in HTML, MHTML o EPUB. Il valore predefinito è`falso` . |
| [ExportDropDownFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exportdropdownformfieldastext/) { get; set; } | Controlla il modo in cui i campi del modulo a discesa vengono salvati in HTML o MHTML. Il valore predefinito è`falso` . |
| [ExportFontResources](../../aspose.words.saving/htmlsaveoptions/exportfontresources/) { get; set; } | Specifica se le risorse dei caratteri devono essere esportate in HTML, MHTML o EPUB. L'impostazione predefinita è`falso` . |
| [ExportFontsAsBase64](../../aspose.words.saving/htmlsaveoptions/exportfontsasbase64/) { get; set; } | Specifica se le risorse dei caratteri devono essere incorporate nell'HTML nella codifica Base64. L'impostazione predefinita è`falso` . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quando`VERO` , fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è`VERO` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/htmlsaveoptions/exportheadersfootersmode/) { get; set; } | Specifica la modalità di output di intestazioni e piè di pagina in HTML, MHTML o EPUB. Il valore predefinito èPerSection per HTML/MHTML eNone per EPUB. |
| [ExportImagesAsBase64](../../aspose.words.saving/htmlsaveoptions/exportimagesasbase64/) { get; set; } | Specifica se le immagini vengono salvate in formato Base64 nell'output HTML, MHTML o EPUB. L'impostazione predefinita è`falso` . |
| [ExportLanguageInformation](../../aspose.words.saving/htmlsaveoptions/exportlanguageinformation/) { get; set; } | Specifica se le informazioni sulla lingua vengono esportate in HTML, MHTML o EPUB. L'impostazione predefinita è`falso` . |
| [ExportListLabels](../../aspose.words.saving/htmlsaveoptions/exportlistlabels/) { get; set; } | Controlla il modo in cui le etichette degli elenchi vengono inviate in HTML, MHTML o EPUB. Il valore predefinito èAuto . |
| [ExportOriginalUrlForLinkedImages](../../aspose.words.saving/htmlsaveoptions/exportoriginalurlforlinkedimages/) { get; set; } | Specifica se l'URL originale deve essere utilizzato come URL delle immagini collegate. Il valore predefinito è`falso` . |
| [ExportPageMargins](../../aspose.words.saving/htmlsaveoptions/exportpagemargins/) { get; set; } | Specifica se i margini della pagina vengono esportati in HTML, MHTML o EPUB. L'impostazione predefinita è`falso` . |
| [ExportPageSetup](../../aspose.words.saving/htmlsaveoptions/exportpagesetup/) { get; set; } | Specifica se l'impostazione della pagina viene esportata in HTML, MHTML o EPUB. L'impostazione predefinita è`falso` . |
| [ExportRelativeFontSize](../../aspose.words.saving/htmlsaveoptions/exportrelativefontsize/) { get; set; } | Specifica se le dimensioni dei caratteri devono essere visualizzate in unità relative durante il salvataggio in HTML, MHTML o EPUB. L'impostazione predefinita è`falso` . |
| [ExportRoundtripInformation](../../aspose.words.saving/htmlsaveoptions/exportroundtripinformation/) { get; set; } | Specifica se scrivere le informazioni di andata e ritorno durante il salvataggio in HTML, MHTML o EPUB. Il valore predefinito è`VERO` per HTML e`falso` per MHTML ed EPUB. |
| [ExportShapesAsSvg](../../aspose.words.saving/htmlsaveoptions/exportshapesassvg/) { get; set; } | Controlla se[`Shape`](../../aspose.words.drawing/shape/) nodi vengono convertiti in immagini SVG quando si salva in HTML, MHTML, EPUB o AZW3. Il valore predefinito è`falso` . |
| [ExportTextInputFormFieldAsText](../../aspose.words.saving/htmlsaveoptions/exporttextinputformfieldastext/) { get; set; } | Controlla il modo in cui i campi del modulo di input testo vengono salvati in HTML o MHTML. Il valore predefinito è`falso` . |
| [ExportTocPageNumbers](../../aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/) { get; set; } | Specifica se scrivere i numeri di pagina nel sommario durante il salvataggio di HTML, MHTML ed EPUB. Il valore predefinito è`falso` . |
| [ExportXhtmlTransitional](../../aspose.words.saving/htmlsaveoptions/exportxhtmltransitional/) { get; set; } | Specifica se scrivere la dichiarazione DOCTYPE durante il salvataggio in HTML o MHTML. Quando`VERO` , scrive una dichiarazione DOCTYPE nel documento prima dell'elemento root. Il valore predefinito è`falso`. Quando si salva in EPUB o HTML5 (Html5 ) viene sempre scritta la dichiarazione DOCTYPE . |
| [FontResourcesSubsettingSizeThreshold](../../aspose.words.saving/htmlsaveoptions/fontresourcessubsettingsizethreshold/) { get; set; } | Controlla quali risorse di carattere necessitano di sottoinsiemi durante il salvataggio in HTML, MHTML o EPUB. L'impostazione predefinita è`0` . |
| [FontSavingCallback](../../aspose.words.saving/htmlsaveoptions/fontsavingcallback/) { get; set; } | Permette di controllare come vengono salvati i caratteri quando un documento viene salvato in HTML, MHTML o EPUB. |
| [FontsFolder](../../aspose.words.saving/htmlsaveoptions/fontsfolder/) { get; set; } | Specifica la cartella fisica in cui vengono salvati i caratteri durante l'esportazione di un documento in HTML. L'impostazione predefinita è una stringa vuota. |
| [FontsFolderAlias](../../aspose.words.saving/htmlsaveoptions/fontsfolderalias/) { get; set; } | Specifica il nome della cartella utilizzata per costruire gli URI dei caratteri scritti in un documento HTML. Il valore predefinito è una stringa vuota. |
| [HtmlVersion](../../aspose.words.saving/htmlsaveoptions/htmlversion/) { get; set; } | Specifica la versione dello standard HTML da utilizzare quando si salva il documento in HTML o MHTML. Il valore predefinito èXhtml . |
| [ImageResolution](../../aspose.words.saving/htmlsaveoptions/imageresolution/) { get; set; } | Specifica la risoluzione di output per le immagini durante l'esportazione in HTML, MHTML o EPUB. L'impostazione predefinita è`96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/htmlsaveoptions/imagesavingcallback/) { get; set; } | Permette di controllare come vengono salvate le immagini quando un documento viene salvato in HTML, MHTML o EPUB. |
| [ImagesFolder](../../aspose.words.saving/htmlsaveoptions/imagesfolder/) { get; set; } | Specifica la cartella fisica in cui vengono salvate le immagini durante l'esportazione di un documento in formato HTML. Il valore predefinito è una stringa vuota. |
| [ImagesFolderAlias](../../aspose.words.saving/htmlsaveoptions/imagesfolderalias/) { get; set; } | Specifica il nome della cartella utilizzata per costruire gli URI di immagine scritti in un documento HTML. Il valore predefinito è una stringa vuota. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli oggetti input penna (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta un valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è`falso` . |
| [MetafileFormat](../../aspose.words.saving/htmlsaveoptions/metafileformat/) { get; set; } | Specifica in quale formato vengono salvati i metafile durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito èPng , il che significa che i metafile vengono sottoposti a rendering in immagini PNG raster. |
| [NavigationMapLevel](../../aspose.words.saving/htmlsaveoptions/navigationmaplevel/) { get; set; } | Specifica il livello massimo di intestazioni inserite nella mappa di navigazione durante l'esportazione nei formati EPUB, MOBI o AZW3 . Il valore predefinito è`3` . |
| [OfficeMathOutputMode](../../aspose.words.saving/htmlsaveoptions/officemathoutputmode/) { get; set; } | Controlla il modo in cui gli oggetti OfficeMath vengono esportati in HTML, MHTML o EPUB. Il valore predefinito èImage . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` formati di output graziosi dove applicabile. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Chiamato durante il salvataggio di un documento e accetta i dati sull'avanzamento del salvataggio. |
| [ResolveFontNames](../../aspose.words.saving/htmlsaveoptions/resolvefontnames/) { get; set; } | Specifica se i nomi delle famiglie di caratteri utilizzati nel documento vengono risolti e sostituiti in base a [`FontSettings`](../../aspose.words/document/fontsettings/) quando viene scritto in formati basati su HTML. |
| [ResourceFolder](../../aspose.words.saving/htmlsaveoptions/resourcefolder/) { get; set; } | Specifica una cartella fisica in cui vengono salvate tutte le risorse come immagini, caratteri e CSS esterni quando un documento viene esportato in HTML. L'impostazione predefinita è una stringa vuota. |
| [ResourceFolderAlias](../../aspose.words.saving/htmlsaveoptions/resourcefolderalias/) { get; set; } | Specifica il nome della cartella utilizzata per costruire gli URI di tutte le risorse scritte in un documento HTML. Il valore predefinito è una stringa vuota. |
| override [SaveFormat](../../aspose.words.saving/htmlsaveoptions/saveformat/) { get; set; } | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto opzioni di salvataggio. Può essereHtml ,Mhtml ,Epub , Azw3 OMobi . |
| [ScaleImageToShapeSize](../../aspose.words.saving/htmlsaveoptions/scaleimagetoshapesize/) { get; set; } | Specifica se le immagini vengono ridimensionate da Aspose.Words alla dimensione della forma delimitante durante l'esportazione in HTML, MHTML o EPUB. Il valore predefinito è`VERO` . |
| [TableWidthOutputMode](../../aspose.words.saving/htmlsaveoptions/tablewidthoutputmode/) { get; set; } | Controlla il modo in cui la larghezza di tabelle, righe e celle viene esportata in HTML, MHTML o EPUB. Il valore predefinito èAll . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzata durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è`falso` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è`VERO` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'antialiasing per il rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (ovvero lenti). |

### Esempi

Mostra come specificare la cartella per la memorizzazione delle immagini collegate dopo il salvataggio in .html.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

string imagesDir = Path.Combine(ArtifactsDir, "SaveHtmlWithOptions");

if (Directory.Exists(imagesDir))
    Directory.Delete(imagesDir, true);

Directory.CreateDirectory(imagesDir);

// Imposta un'opzione per esportare i campi del modulo come testo normale anziché come elementi di input HTML.
HtmlSaveOptions options = new HtmlSaveOptions(SaveFormat.Html)
{
    ExportTextInputFormFieldAsText = true, 
    ImagesFolder = imagesDir
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveHtmlWithOptions.html", options);
```

Mostra come utilizzare una codifica specifica quando si salva un documento in .epub.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Utilizza un oggetto SaveOptions per specificare la codifica per un documento che salveremo.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Per impostazione predefinita, un documento .epub di output avrà tutto il suo contenuto in una parte HTML.
// Un criterio di suddivisione ci permette di segmentare il documento in più parti HTML.
// Imposteremo i criteri per suddividere il documento in paragrafi di intestazione.
// Ciò è utile per i lettori che non possono leggere file HTML più significativi di una dimensione specifica.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Specifica che vogliamo esportare le proprietà del documento.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

Mostra come dividere un documento in parti e salvarle.

```csharp
public void DocumentPartsFileNames()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    string outFileName = "SavingCallback.DocumentPartsFileNames.html";

    // Crea un oggetto "HtmlFixedSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui convertiamo il documento in HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Se salviamo il documento normalmente, ci sarà un output HTML
    // documento con tutto il contenuto del documento sorgente.
    // Imposta la proprietà "DocumentSplitCriteria" su "DocumentSplitCriteria.SectionBreak" su
    // salva il nostro documento in più file HTML: uno per ogni sezione.
    options.DocumentSplitCriteria = DocumentSplitCriteria.SectionBreak;

    // Assegna un callback personalizzato alla proprietà "DocumentPartSavingCallback" per modificare la logica di salvataggio della parte del documento.
    options.DocumentPartSavingCallback = new SavedDocumentPartRename(outFileName, options.DocumentSplitCriteria);

    // Se convertiamo un documento che contiene immagini in html, ci ritroveremo con un file html che collega a diverse immagini.
    // Ogni immagine avrà la forma di un file nel file system locale.
    // Esiste anche un callback che può personalizzare il nome e la posizione del file system di ciascuna immagine.
    options.ImageSavingCallback = new SavedImageRename(outFileName);

    doc.Save(ArtifactsDir + outFileName, options);
}

/// <summary>
/// Imposta nomi di file personalizzati per i documenti di output in cui l'operazione di salvataggio divide un documento.
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
        // Possiamo accedere all'intero documento sorgente tramite la proprietà "Document".
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

        // Di seguito sono riportati due modi per specificare dove Aspose.Words salverà ciascuna parte del documento.
        // 1 - Imposta un nome file per il file della parte di output:
        args.DocumentPartFileName = partFileName;

        // 2 - Crea un flusso personalizzato per il file della parte di output:
        args.DocumentPartStream = new FileStream(ArtifactsDir + partFileName, FileMode.Create);

        Assert.True(args.DocumentPartStream.CanWrite);
        Assert.False(args.KeepDocumentPartStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
    private readonly DocumentSplitCriteria mDocumentSplitCriteria;
}

/// <summary>
/// Imposta nomi di file personalizzati per i file di immagine creati da una conversione HTML.
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

        // Di seguito sono riportati due modi per specificare dove Aspose.Words salverà ciascuna parte del documento.
        // 1 - Imposta un nome file per il file immagine di output:
        args.ImageFileName = imageFileName;

        // 2 - Crea un flusso personalizzato per il file immagine di output:
        args.ImageStream = new FileStream(ArtifactsDir + imageFileName, FileMode.Create);

        Assert.True(args.ImageStream.CanWrite);
        Assert.True(args.IsImageAvailable);
        Assert.False(args.KeepImageStreamOpen);
    }

    private int mCount;
    private readonly string mOutFileName;
}
```

### Guarda anche

* class [SaveOptions](../saveoptions/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


