---
title: MarkdownSaveOptions Class
linktitle: MarkdownSaveOptions
articleTitle: MarkdownSaveOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Saving.MarkdownSaveOptions per un salvataggio avanzato dei documenti in formato Markdown. Personalizza il tuo output con opzioni avanzate oggi stesso!
type: docs
weight: 6060
url: /it/net/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class

Classe per specificare opzioni aggiuntive durante il salvataggio di un documento inMarkdown formato.

Per saperne di più, visita il[Specificare le opzioni di salvataggio](https://docs.aspose.com/words/net/specify-save-options/) articolo di documentazione.

```csharp
public class MarkdownSaveOptions : TxtSaveOptionsBase
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [MarkdownSaveOptions](markdownsaveoptions/)() | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nelMarkdown formato. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è`falso` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso al modello predefinito (incluso il nome del file). Il valore predefinito per questa proprietà è**stringa vuota** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [EmptyParagraphExportMode](../../aspose.words.saving/markdownsaveoptions/emptyparagraphexportmode/) { get; set; } | Specifica come esportare i paragrafi vuoti in Markdown. Il valore predefinito èEmptyLine . |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Specifica la codifica da utilizzare durante l'esportazione in formati di testo. Il valore predefinito è **Codifica.UTF8** . |
| [ExportAsHtml](../../aspose.words.saving/markdownsaveoptions/exportashtml/) { get; set; } | Consente di specificare gli elementi da esportare in Markdown come HTML grezzo. Il valore predefinito èNone . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quando`VERO` , fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è`VERO` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Specifica il modo in cui le intestazioni e i piè di pagina vengono esportati nei formati di testo. Il valore predefinito èPrimaryOnly . |
| [ExportImagesAsBase64](../../aspose.words.saving/markdownsaveoptions/exportimagesasbase64/) { get; set; } | Specifica se le immagini vengono salvate in formato Base64 nel file di output. Il valore predefinito è`falso` . |
| [ExportUnderlineFormatting](../../aspose.words.saving/markdownsaveoptions/exportunderlineformatting/) { get; set; } | Ottiene o imposta un valore booleano che indica di esportare la formattazione del testo sottolineato come sequenza di due caratteri più "++". Il valore predefinito è`falso` . |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Consente di specificare se le interruzioni di pagina devono essere mantenute durante l'esportazione. |
| [ImageResolution](../../aspose.words.saving/markdownsaveoptions/imageresolution/) { get; set; } | Specifica la risoluzione di output per le immagini durante l'esportazione in Markdown. Il valore predefinito è`96 dpi` . |
| [ImageSavingCallback](../../aspose.words.saving/markdownsaveoptions/imagesavingcallback/) { get; set; } | Consente di controllare come vengono salvate le immagini quando un documento viene salvato su Markdown formato. |
| [ImagesFolder](../../aspose.words.saving/markdownsaveoptions/imagesfolder/) { get; set; } | Specifica la cartella fisica in cui vengono salvate le immagini quando si esporta un documento in Markdown formato. Il valore predefinito è una stringa vuota. |
| [ImagesFolderAlias](../../aspose.words.saving/markdownsaveoptions/imagesfolderalias/) { get; set; } | Specifica il nome della cartella utilizzata per costruire gli URI delle immagini scritti in un documento. Il valore predefinito è una stringa vuota. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti ink (InkML). |
| [LinkExportMode](../../aspose.words.saving/markdownsaveoptions/linkexportmode/) { get; set; } | Specifica come i collegamenti verranno scritti nel file di output. Il valore predefinito èAuto . |
| [ListExportMode](../../aspose.words.saving/markdownsaveoptions/listexportmode/) { get; set; } | Specifica come gli elementi dell'elenco verranno scritti nel file di output. Il valore predefinito èMarkdownSyntax . |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è`falso` . |
| [OfficeMathExportMode](../../aspose.words.saving/markdownsaveoptions/officemathexportmode/) { get; set; } | Specifica come OfficeMath verrà scritto nel file di output. Il valore predefinito èText . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Specifica la stringa da utilizzare come interruzione di paragrafo durante l'esportazione in formati di testo. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formatta bene l'output dove applicabile. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Viene chiamato durante il salvataggio di un documento e accetta dati sullo stato di avanzamento del salvataggio. |
| override [SaveFormat](../../aspose.words.saving/markdownsaveoptions/saveformat/) { get; set; } | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere soloMarkdown . |
| [TableContentAlignment](../../aspose.words.saving/markdownsaveoptions/tablecontentalignment/) { get; set; } | Ottiene o imposta un valore che specifica come allineare i contenuti nelle tabelle durante l'esportazione inMarkdown format. Il valore predefinito èAuto . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è`null` e non vengono utilizzati file temporanei. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determina se gli attributi del font verranno modificati in base al codice carattere utilizzato. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è`falso` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è`VERO` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (ad esempio lenti). |

## Esempi

Mostra come rinominare l'immagine durante il salvataggio nel documento Markdown.

```csharp
public void RenameImages()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
    // Se convertiamo in Markdown un documento contenente immagini, otterremo un file Markdown che rimanda a più immagini.
    // Ogni immagine sarà sotto forma di file nel file system locale.
    // Esiste anche una callback che può personalizzare il nome e la posizione del file system di ciascuna immagine.
    saveOptions.ImageSavingCallback = new SavedImageRename("MarkdownSaveOptions.HandleDocument.md");
    saveOptions.SaveFormat = SaveFormat.Markdown;

    // In questo momento verrà eseguito il metodo ImageSaving() del nostro callback.
    doc.Save(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md", saveOptions);

    Assert.AreEqual(1,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".jpeg")));
    Assert.AreEqual(8,
        Directory.GetFiles(ArtifactsDir)
            .Where(s => s.StartsWith(ArtifactsDir + "MarkdownSaveOptions.HandleDocument.md shape"))
            .Count(f => f.EndsWith(".png")));
}

/// <summary>
/// Rinomina le immagini salvate prodotte quando si salva un documento Markdown.
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

        args.ImageFileName = imageFileName;
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

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
