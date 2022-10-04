---
title: HtmlFixedSaveOptions
second_title: Aspose.Words per .NET API Reference
description: Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento nel fileHtmlFixed formato.
type: docs
weight: 4820
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento nel fileHtmlFixed formato.

```csharp
public class HtmlFixedSaveOptions : FixedPageSaveOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [HtmlFixedSaveOptions](htmlfixedsaveoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di caratteri con contorni PostScript quando l'incorporamento di caratteri TrueType in un documento viene salvato. Il valore predefinito è **falso** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering dei colori. |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/) { get; set; } | Specifica il prefisso che viene aggiunto a tutti i nomi delle classi nel file style.css. Il valore predefinito è`"ah"` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **stringa vuota** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering delle forme DrawingML. |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding/) { get; set; } | Specifica la codifica da utilizzare durante l'esportazione in HTML. Il valore predefinito è`nuova codifica UTF8(true)` (UTF-8 con distinta base). |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/) { get; set; } | Specifica se il CSS (Cascading Style Sheet) deve essere incorporato nel documento HTML. |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/) { get; set; } | Specifica se i caratteri devono essere incorporati nel documento HTML in formato Base64. Nota l'impostazione di questo flag può aumentare notevolmente le dimensioni del file HTML di output. |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/) { get; set; } | Specifica se le immagini devono essere incorporate nel documento HTML in formato Base64. Nota l'impostazione di questo flag può aumentare notevolmente le dimensioni del file HTML di output. |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/) { get; set; } | Specifica se le risorse SVG devono essere incorporate nel documento HTML. Il valore predefinito è`VERO` . |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields/) { get; set; } | Ottiene o imposta l'indicazione se i campi del modulo vengono esportati come elementi interattivi (come tag 'input') anziché convertiti in testo o grafica. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Se true, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **VERO** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Ottiene o imposta un valore che determina i formati di documento in base ai quali è consentito mappare[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo per impostazione predefinitaFlatOpc il formato del documento può essere mappato. |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat/) { get; set; } | Ottiene o imposta[`ExportFontFormat`](../exportfontformat/) utilizzato per l'esportazione dei caratteri. Il valore predefinito èWoff . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli oggetti Ink (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento Html. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se eseguire l'ottimizzazione della memoria prima di salvare il documento. Il valore predefinito per questa proprietà è **falso** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Consente di specificare le opzioni di rendering del metafile. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Ottiene o imposta[`NumeralFormat`](../numeralformat/) utilizzato per il rendering dei numeri. I numeri europei vengono utilizzati per impostazione predefinita. |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/) { get; set; } | Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, anche i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere compromessa se questa proprietà è impostata su true. L'impostazione predefinita è true. |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/) { get; set; } | Specifica l'allineamento orizzontale delle pagine in un documento HTML. Il valore predefinito è`HtmlFixedHorizontalPageAlignment.Center` . |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins/) { get; set; } | Specifica i margini intorno alle pagine in un documento HTML. Il valore dei margini è misurato in punti e deve essere uguale o maggiore di 0. Il valore predefinito è 10 punti. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Consente di controllare come vengono salvate le pagine separate quando un documento viene esportato in un formato pagina fisso. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Ottiene o imposta le pagine di cui eseguire il rendering. Il valore predefinito è tutte le pagine nel documento. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formati graziosi di output ove applicabile. Il valore predefinito è **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Chiamato durante il salvataggio di un documento e accetta i dati sull'avanzamento del salvataggio. |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback/) { get; set; } | Consente di controllare come vengono salvate le risorse (immagini, font e css) quando un documento viene esportato in formato Html a pagina fissa. |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/) { get; set; } | Specifica la cartella fisica in cui vengono salvate le risorse (immagini, caratteri, CSS) durante l'esportazione di un documento in formato Html. L'impostazione predefinita è`nullo` . |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias/) { get; set; } | Specifica il nome della cartella utilizzata per costruire gli URI di immagine scritti in un documento Html. L'impostazione predefinita è`nullo` . |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/) { get; set; } | Il flag indica se le regole CSS "@font-face" devono essere inserite in un file separato "fontFaces.css" quando un documento viene salvato con un foglio di stile esterno (ovvero, quando[`ExportEmbeddedCss`](./exportembeddedcss/) è`falso` ). Il valore predefinito è`falso` , tutte le regole CSS sono scritte in un unico file "styles.css". |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat/) { get; set; } | Specifica il formato in cui verrà salvato il documento se viene utilizzato questo oggetto opzioni di salvataggio. Può essereHtmlFixed . |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder/) { get; set; } | Specifica se deve essere visualizzato il bordo attorno alle pagine. L'impostazione predefinita è`VERO` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzata durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è **VERO** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Ottiene o imposta il valore che determina se il contenuto di[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) viene aggiornato prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-alias per il rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (cioè lenti). |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/) { get; set; } | Flag indica se i caratteri della macchina di destinazione devono essere utilizzati per visualizzare il documento. Se questo flag è impostato su true,[`FontFormat`](./fontformat/) e[`ExportEmbeddedFonts`](./exportembeddedfonts/)le proprietà non hanno effetto, anche [`ResourceSavingCallback`](./resourcesavingcallback/) non viene attivato per i caratteri. L'impostazione predefinita è false. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |

### Esempi

Mostra come utilizzare un callback per stampare gli URI di risorse esterne create durante la conversione di un documento in HTML.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // Una cartella specificata da ResourcesFolderAlias conterrà le risorse invece di ResourcesFolder.
    // Dobbiamo assicurarci che la cartella esista prima che gli stream possano inserirvi le proprie risorse.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Conta e stampa gli URI delle risorse contenute in quando vengono convertiti in HTML fisso.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Se impostiamo un alias di cartella nell'oggetto SaveOptions, saremo in grado di stamparlo da qui.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Per impostazione predefinita, 'ResourceFileUri' utilizza la cartella di sistema per i caratteri.
                // Per evitare problemi su altre piattaforme è necessario specificare in modo esplicito il percorso dei caratteri.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Se abbiamo specificato una cartella nella proprietà "ResourcesFolderAlias",
        // dovremo anche reindirizzare ogni flusso per mettere la sua risorsa in quella cartella.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### Guarda anche

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
