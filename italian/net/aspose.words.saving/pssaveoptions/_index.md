---
title: PsSaveOptions Class
linktitle: PsSaveOptions
articleTitle: PsSaveOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.Saving.PsSaveOptions per migliorare la tua esperienza di salvataggio dei documenti in formato Ps con opzioni personalizzabili per risultati ottimali.
type: docs
weight: 6350
url: /it/net/aspose.words.saving/pssaveoptions/
---
## PsSaveOptions class

Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento inPs formato.

Per saperne di più, visita il[Specificare le opzioni di salvataggio](https://docs.aspose.com/words/net/specify-save-options/) articolo di documentazione.

```csharp
public class PsSaveOptions : FixedPageSaveOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PsSaveOptions](pssaveoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è`falso` . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Ottiene o imposta un valore che determina come vengono resi i colori. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso al modello predefinito (incluso il nome del file). Il valore predefinito per questa proprietà è**stringa vuota** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quando`VERO` , fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è`VERO` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti ink (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality/) { get; set; } | Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento HTML. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è`falso` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Consente di specificare le opzioni di rendering dei metafile. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Ottiene o imposta[`NumeralFormat`](../numeralformat/) utilizzato per il rendering dei numeri. Per impostazione predefinita vengono utilizzati i numeri europei. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, anche i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere influenzata se questa proprietà è impostata su`VERO` . Il valore predefinito è`falso` . |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Consente di controllare come vengono salvate le singole pagine quando un documento viene esportato in un formato di pagina fisso. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Ottiene o imposta le pagine da visualizzare. L'impostazione predefinita è tutte le pagine del documento. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formatta bene l'output dove applicabile. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Viene chiamato durante il salvataggio di un documento e accetta dati sullo stato di avanzamento del salvataggio. |
| override [SaveFormat](../../aspose.words.saving/pssaveoptions/saveformat/) { get; set; } | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere soloPs . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è`null` e non vengono utilizzati file temporanei. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determina se gli attributi del font verranno modificati in base al codice carattere utilizzato. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è`falso` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è`VERO` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pssaveoptions/usebookfoldprintingsettings/) { get; set; } | Ottiene o imposta un valore booleano che indica se il documento deve essere salvato utilizzando un layout di stampa opuscolo, se specificato tramite[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (ad esempio lenti). |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |

## Esempi

Mostra come salvare un documento nel formato Postscript sotto forma di piega a libro.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

// Creiamo un oggetto "PsSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in PostScript.
// Imposta la proprietà "UseBookFoldPrintingSettings" su "true" per organizzare il contenuto
// nel documento Postscript di output in un modo che ci aiuti a trasformarlo in un opuscolo.
// Impostare la proprietà "UseBookFoldPrintingSettings" su "false" per salvare il documento normalmente.
PsSaveOptions saveOptions = new PsSaveOptions
{
    SaveFormat = SaveFormat.Ps,
    UseBookFoldPrintingSettings = renderTextAsBookFold
};

// Se stiamo rendendo il documento come un opuscolo, dobbiamo impostare "MultiplePages"
// proprietà degli oggetti di impostazione pagina di tutte le sezioni su "MultiplePagesType.BookFoldPrinting".
foreach (Section s in doc.Sections)
{
    s.PageSetup.MultiplePages = MultiplePagesType.BookFoldPrinting;
}

// Una volta stampato questo documento su entrambi i lati delle pagine, possiamo piegare tutte le pagine a metà contemporaneamente,
// e i contenuti si allineeranno in modo da creare un opuscolo.
doc.Save(ArtifactsDir + "PsSaveOptions.UseBookFoldPrintingSettings.ps", saveOptions);
```

### Guarda anche

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
