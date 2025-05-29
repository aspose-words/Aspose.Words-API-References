---
title: HtmlFixedSaveOptions Class
linktitle: HtmlFixedSaveOptions
articleTitle: HtmlFixedSaveOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Saving.HtmlFixedSaveOptions per migliorare la tua esperienza di salvataggio dei documenti. Personalizza le impostazioni per un output ottimale in formato HtmlFixed.
type: docs
weight: 5830
url: /it/net/aspose.words.saving/htmlfixedsaveoptions/
---
## HtmlFixedSaveOptions class

Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento inHtmlFixed formato.

Per saperne di più, visita il[Specificare le opzioni di salvataggio](https://docs.aspose.com/words/net/specify-save-options/) articolo di documentazione.

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
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è`falso` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Ottiene o imposta un valore che determina come vengono resi i colori. |
| [CssClassNamesPrefix](../../aspose.words.saving/htmlfixedsaveoptions/cssclassnamesprefix/) { get; set; } | Specifica il prefisso che viene aggiunto a tutti i nomi di classe nel file style.css. Il valore predefinito è`"oh"` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso al modello predefinito (incluso il nome del file). Il valore predefinito per questa proprietà è**stringa vuota** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [Encoding](../../aspose.words.saving/htmlfixedsaveoptions/encoding/) { get; set; } | Specifica la codifica da utilizzare durante l'esportazione in HTML. Il valore predefinito è`nuova codifica UTF8(vero)` (UTF-8 con BOM). |
| [ExportEmbeddedCss](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/) { get; set; } | Specifica se il CSS (Cascading Style Sheet) deve essere incorporato nel documento HTML. |
| [ExportEmbeddedFonts](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/) { get; set; } | Specifica se i font devono essere incorporati nel documento HTML in formato Base64. Nota: l'impostazione di questo flag può aumentare significativamente la dimensione del file HTML di output. |
| [ExportEmbeddedImages](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedimages/) { get; set; } | Specifica se le immagini devono essere incorporate nel documento HTML in formato Base64. Nota: l'impostazione di questo flag può aumentare significativamente la dimensione del file HTML di output. |
| [ExportEmbeddedSvg](../../aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/) { get; set; } | Specifica se le risorse SVG devono essere incorporate nel documento HTML. Il valore predefinito è`VERO` . |
| [ExportFormFields](../../aspose.words.saving/htmlfixedsaveoptions/exportformfields/) { get; set; } | Ottiene o imposta l'indicazione se i campi del modulo vengono esportati come elementi interattivi (come tag 'input') anziché convertiti in testo o grafica. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quando`VERO` , fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è`VERO` . |
| [FontFormat](../../aspose.words.saving/htmlfixedsaveoptions/fontformat/) { get; set; } | Ottiene o imposta[`ExportFontFormat`](../exportfontformat/) utilizzato per l'esportazione dei font. Il valore predefinito èWoff . |
| [IdPrefix](../../aspose.words.saving/htmlfixedsaveoptions/idprefix/) { get; set; } | Specifica un prefisso da aggiungere a tutti gli ID degli elementi generati nel documento di output. Il valore predefinito è null e non viene aggiunto alcun prefisso. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti ink (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento HTML. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è`falso` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Consente di specificare le opzioni di rendering dei metafile. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Ottiene o imposta[`NumeralFormat`](../numeralformat/) utilizzato per il rendering dei numeri. Per impostazione predefinita vengono utilizzati i numeri europei. |
| override [OptimizeOutput](../../aspose.words.saving/htmlfixedsaveoptions/optimizeoutput/) { get; set; } | Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, anche i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere influenzata se questa proprietà è impostata su`VERO` . Il valore predefinito è`VERO` . |
| [PageHorizontalAlignment](../../aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/) { get; set; } | Specifica l'allineamento orizzontale delle pagine in un documento HTML. Il valore predefinito èCenter . |
| [PageMargins](../../aspose.words.saving/htmlfixedsaveoptions/pagemargins/) { get; set; } | Specifica i margini attorno alle pagine in un documento HTML. Il valore dei margini è misurato in punti e deve essere uguale o maggiore di 0. Il valore predefinito è 10 punti. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Consente di controllare come vengono salvate le singole pagine quando un documento viene esportato in un formato di pagina fisso. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Ottiene o imposta le pagine da visualizzare. L'impostazione predefinita è tutte le pagine del documento. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formatta bene l'output dove applicabile. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Viene chiamato durante il salvataggio di un documento e accetta dati sullo stato di avanzamento del salvataggio. |
| [RemoveJavaScriptFromLinks](../../aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/) { get; set; } | Specifica se JavaScript verrà rimosso dai collegamenti. Il valore predefinito è`falso` . |
| [ResourceSavingCallback](../../aspose.words.saving/htmlfixedsaveoptions/resourcesavingcallback/) { get; set; } | Consente di controllare come vengono salvate le risorse (immagini, caratteri e css) quando un documento viene esportato nel formato HTML a pagina fissa. |
| [ResourcesFolder](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolder/) { get; set; } | Specifica la cartella fisica in cui vengono salvate le risorse (immagini, caratteri, css) quando si esporta un documento in formato Html. Il valore predefinito è`null` . |
| [ResourcesFolderAlias](../../aspose.words.saving/htmlfixedsaveoptions/resourcesfolderalias/) { get; set; } | Specifica il nome della cartella utilizzata per costruire gli URI delle immagini scritti in un documento HTML. Il valore predefinito è`null` . |
| [SaveFontFaceCssSeparately](../../aspose.words.saving/htmlfixedsaveoptions/savefontfacecssseparately/) { get; set; } | Il flag indica se le regole CSS "@font-face" devono essere inserite in un file separato "fontFaces.css" quando un documento viene salvato con un foglio di stile esterno (ovvero, quando[`ExportEmbeddedCss`](./exportembeddedcss/) è`falso` ). Il valore predefinito è`falso` , tutte le regole CSS sono scritte in un singolo file "styles.css". |
| override [SaveFormat](../../aspose.words.saving/htmlfixedsaveoptions/saveformat/) { get; set; } | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere soloHtmlFixed . |
| [ShowPageBorder](../../aspose.words.saving/htmlfixedsaveoptions/showpageborder/) { get; set; } | Specifica se il bordo attorno alle pagine deve essere visualizzato. Il valore predefinito è`VERO` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è`null` e non vengono utilizzati file temporanei. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determina se gli attributi del font verranno modificati in base al codice carattere utilizzato. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è`falso` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è`VERO` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (ad esempio lenti). |
| [UseTargetMachineFonts](../../aspose.words.saving/htmlfixedsaveoptions/usetargetmachinefonts/) { get; set; } | Il flag indica se i font della macchina di destinazione devono essere utilizzati per visualizzare il documento. Se questo flag è impostato su`VERO` ,[`FontFormat`](./fontformat/) E[`ExportEmbeddedFonts`](./exportembeddedfonts/) le proprietà non hanno effetto, anche[`ResourceSavingCallback`](./resourcesavingcallback/) non viene attivato per i font. Il valore predefinito è`falso` . |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |

## Esempi

Mostra come utilizzare un callback per stampare gli URI delle risorse esterne create durante la conversione di un documento in HTML.

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

    // Una cartella specificata da ResourcesFolderAlias conterrà le risorse anziché ResourcesFolder.
    // Dobbiamo assicurarci che la cartella esista prima che i flussi possano inserirvi le loro risorse.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Conta e stampa gli URI delle risorse contenute da mentre vengono convertiti in HTML fisso.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Se impostiamo un alias di cartella nell'oggetto SaveOptions, potremo stamparlo da qui.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // Per impostazione predefinita, 'ResourceFileUri' utilizza la cartella di sistema per i font.
                // Per evitare problemi su altre piattaforme è necessario specificare esplicitamente il percorso per i font.
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
