---
title: XamlFixedSaveOptions
second_title: Aspose.Words per .NET API Reference
description: Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento nel fileXamlFixed formato.
type: docs
weight: 5410
url: /it/net/aspose.words.saving/xamlfixedsaveoptions/
---
## XamlFixedSaveOptions class

Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento nel fileXamlFixed formato.

```csharp
public class XamlFixedSaveOptions : FixedPageSaveOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [XamlFixedSaveOptions](xamlfixedsaveoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di caratteri con contorni PostScript quando l'incorporamento di caratteri TrueType in un documento viene salvato. Il valore predefinito è **falso** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering dei colori. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **stringa vuota** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering delle forme DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Se true, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **VERO** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Ottiene o imposta un valore che determina i formati di documento in base ai quali è consentito mappare[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo per impostazione predefinitaFlatOpc il formato del documento può essere mappato. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli oggetti Ink (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento Html. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se eseguire l'ottimizzazione della memoria prima di salvare il documento. Il valore predefinito per questa proprietà è **falso** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Consente di specificare le opzioni di rendering del metafile. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Ottiene o imposta[`NumeralFormat`](../numeralformat/) utilizzato per il rendering dei numeri. I numeri europei vengono utilizzati per impostazione predefinita. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, anche i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere compromessa se questa proprietà è impostata su true. L'impostazione predefinita è false. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Consente di controllare come vengono salvate le pagine separate quando un documento viene esportato in un formato pagina fisso. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Ottiene o imposta le pagine di cui eseguire il rendering. Il valore predefinito è tutte le pagine nel documento. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formati graziosi di output ove applicabile. Il valore predefinito è **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Chiamato durante il salvataggio di un documento e accetta i dati sull'avanzamento del salvataggio. |
| [ResourceSavingCallback](../../aspose.words.saving/xamlfixedsaveoptions/resourcesavingcallback/) { get; set; } | Consente di controllare come vengono salvate le risorse (immagini e caratteri) quando un documento viene esportato in formato Xaml a pagina fissa. |
| [ResourcesFolder](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolder/) { get; set; } | Specifica la cartella fisica in cui vengono salvate le risorse (immagini e caratteri) durante l'esportazione di un documento in formato Xaml a pagina fissa. L'impostazione predefinita è`nullo` . |
| [ResourcesFolderAlias](../../aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/) { get; set; } | Specifica il nome della cartella utilizzata per costruire URI immagine scritti in un documento Xaml a pagina fissa. Il valore predefinito è`nullo` . |
| override [SaveFormat](../../aspose.words.saving/xamlfixedsaveoptions/saveformat/) { get; set; } | Specifica il formato in cui verrà salvato il documento se viene utilizzato questo oggetto opzioni di salvataggio. Può essereXamlFixed . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzata durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è **VERO** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Ottiene o imposta il valore che determina se il contenuto di[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) viene aggiornato prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-alias per il rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (cioè lenti). |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(object) | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |

### Esempi

Mostra come stampare gli URI delle risorse collegate create durante la conversione di un documento in .xaml in formato fisso.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Crea un oggetto "XamlFixedSaveOptions", che possiamo passare al metodo "Save" del documento
    // per modificare il modo in cui salviamo il documento nel formato di salvataggio XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Utilizzare la proprietà "ResourcesFolder" per assegnare una cartella nel file system locale in cui
    // Aspose.Words salverà tutte le risorse collegate del documento, come immagini e caratteri.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Utilizzare la proprietà "ResourcesFolderAlias" per utilizzare questa cartella
    // durante la creazione di URI di immagine invece del nome della cartella delle risorse.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // Una cartella specificata da "ResourcesFolderAlias" dovrà contenere le risorse invece di "ResourcesFolder".
    // Dobbiamo assicurarci che la cartella esista prima che i flussi di callback possano inserirvi le proprie risorse.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// Conta e stampa gli URI delle risorse create durante la conversione in .xaml fisso.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // Se avessimo specificato un alias per la cartella delle risorse, avremmo anche bisogno
        // per reindirizzare ogni flusso per inserire la sua risorsa nella cartella alias.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Guarda anche

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
