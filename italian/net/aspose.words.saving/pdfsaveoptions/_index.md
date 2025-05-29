---
title: PdfSaveOptions Class
linktitle: PdfSaveOptions
articleTitle: PdfSaveOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.PdfSaveOptions per migliorare la tua esperienza di salvataggio dei documenti. Personalizza le impostazioni per ottenere la migliore qualità e prestazioni di output PDF.
type: docs
weight: 6320
url: /it/net/aspose.words.saving/pdfsaveoptions/
---
## PdfSaveOptions class

Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento inPdf formato.

Per saperne di più, visita il[Specificare le opzioni di salvataggio](https://docs.aspose.com/words/net/specify-save-options/) articolo di documentazione.

```csharp
public class PdfSaveOptions : FixedPageSaveOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PdfSaveOptions](pdfsaveoptions/)() | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento in Pdf formato. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AdditionalTextPositioning](../../aspose.words.saving/pdfsaveoptions/additionaltextpositioning/) { get; set; } | Un flag che specifica se scrivere o meno operatori di posizionamento del testo aggiuntivi. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è`falso` . |
| [AttachmentsEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/attachmentsembeddingmode/) { get; set; } | Ottiene o imposta un valore che determina come gli allegati vengono incorporati nel documento PDF. |
| [CacheBackgroundGraphics](../../aspose.words.saving/pdfsaveoptions/cachebackgroundgraphics/) { get; set; } | Ottiene o imposta un valore che determina se memorizzare o meno nella cache la grafica posizionata sullo sfondo del documento. |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode/) { get; set; } | Ottiene o imposta un valore che determina come vengono resi i colori. |
| [Compliance](../../aspose.words.saving/pdfsaveoptions/compliance/) { get; set; } | Specifica il livello di conformità agli standard PDF per i documenti di output. |
| [CreateNoteHyperlinks](../../aspose.words.saving/pdfsaveoptions/createnotehyperlinks/) { get; set; } | Specifica se convertire i riferimenti alle note a piè di pagina/note di chiusura nel testo principale del racconto in collegamenti ipertestuali attivi. Quando si fa clic, il collegamento ipertestuale porterà alla nota a piè di pagina/nota di chiusura corrispondente. L'impostazione predefinita è`falso` . |
| [CustomPropertiesExport](../../aspose.words.saving/pdfsaveoptions/custompropertiesexport/) { get; set; } | Ottiene o imposta un valore che determina il modo in cui[`CustomDocumentProperties`](../../aspose.words/document/customdocumentproperties/) vengono esportati in file PDF. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso al modello predefinito (incluso il nome del file). Il valore predefinito per questa proprietà è**stringa vuota** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/pdfsaveoptions/digitalsignaturedetails/) { get; set; } | Ottiene o imposta i dettagli per la firma del documento PDF di output. |
| [DisplayDocTitle](../../aspose.words.saving/pdfsaveoptions/displaydoctitle/) { get; set; } | Flag che specifica se la barra del titolo della finestra deve visualizzare il titolo del documento tratto dalla voce Titolo del dizionario delle informazioni sul documento. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| override [DmlEffectsRenderingMode](../../aspose.words.saving/pdfsaveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [DownsampleOptions](../../aspose.words.saving/pdfsaveoptions/downsampleoptions/) { get; set; } | Consente di specificare le opzioni di downsample. |
| [EmbedFullFonts](../../aspose.words.saving/pdfsaveoptions/embedfullfonts/) { get; set; } | Controlla come i font vengono incorporati nei documenti PDF risultanti. |
| [EncryptionDetails](../../aspose.words.saving/pdfsaveoptions/encryptiondetails/) { get; set; } | Ottiene o imposta i dettagli per la crittografia del documento PDF di output. |
| [ExportDocumentStructure](../../aspose.words.saving/pdfsaveoptions/exportdocumentstructure/) { get; set; } | Ottiene o imposta un valore che determina se esportare o meno la struttura del documento. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quando`VERO` , fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è`VERO` . |
| [ExportLanguageToSpanTag](../../aspose.words.saving/pdfsaveoptions/exportlanguagetospantag/) { get; set; } | Ottiene o imposta un valore che determina se creare o meno un tag "Span" nella struttura del documento per esportare la lingua del testo. |
| [ExportParagraphGraphicsToArtifact](../../aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/) { get; set; } | Ottiene o imposta un valore che determina se un'immagine di paragrafo deve essere contrassegnata come artefatto. |
| [FontEmbeddingMode](../../aspose.words.saving/pdfsaveoptions/fontembeddingmode/) { get; set; } | Specifica la modalità di incorporamento del font. |
| [HeaderFooterBookmarksExportMode](../../aspose.words.saving/pdfsaveoptions/headerfooterbookmarksexportmode/) { get; set; } | Determina come vengono esportati i segnalibri nelle intestazioni/piè di pagina. |
| [ImageColorSpaceExportMode](../../aspose.words.saving/pdfsaveoptions/imagecolorspaceexportmode/) { get; set; } | Specifica come verrà selezionato lo spazio colore per le immagini nel documento PDF. |
| [ImageCompression](../../aspose.words.saving/pdfsaveoptions/imagecompression/) { get; set; } | Specifica il tipo di compressione da utilizzare per tutte le immagini nel documento. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti ink (InkML). |
| [InterpolateImages](../../aspose.words.saving/pdfsaveoptions/interpolateimages/) { get; set; } | Un flag che indica se l'interpolazione dell'immagine deve essere eseguita da un lettore conforme. Quando`falso` è specificato, il flag non viene scritto nel documento di output e al suo posto viene utilizzato il comportamento predefinito del lettore. |
| [JpegQuality](../../aspose.words.saving/pdfsaveoptions/jpegquality/) { get; set; } | Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento PDF. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è`falso` . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions/) { get; set; } | Consente di specificare le opzioni di rendering dei metafile. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat/) { get; set; } | Ottiene o imposta[`NumeralFormat`](../numeralformat/) utilizzato per il rendering dei numeri. Per impostazione predefinita vengono utilizzati i numeri europei. |
| [OpenHyperlinksInNewWindow](../../aspose.words.saving/pdfsaveoptions/openhyperlinksinnewwindow/) { get; set; } | Ottiene o imposta un valore che determina se i collegamenti ipertestuali nel documento Pdf di output devono essere forzati ad essere aperti in una nuova finestra (o scheda) di un browser. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput/) { get; set; } | Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, anche i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere influenzata se questa proprietà è impostata su`VERO` . Il valore predefinito è`falso` . |
| [OutlineOptions](../../aspose.words.saving/pdfsaveoptions/outlineoptions/) { get; } | Consente di specificare le opzioni del contorno. |
| [PageLayout](../../aspose.words.saving/pdfsaveoptions/pagelayout/) { get; set; } | Specifica il layout di pagina da utilizzare quando il documento viene aperto in un lettore PDF. |
| [PageMode](../../aspose.words.saving/pdfsaveoptions/pagemode/) { get; set; } | Specifica come deve essere visualizzato il documento PDF quando viene aperto in un lettore PDF. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback/) { get; set; } | Consente di controllare come vengono salvate le singole pagine quando un documento viene esportato in un formato di pagina fisso. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset/) { get; set; } | Ottiene o imposta le pagine da visualizzare. L'impostazione predefinita è tutte le pagine del documento. |
| [PreblendImages](../../aspose.words.saving/pdfsaveoptions/preblendimages/) { get; set; } | Ottiene o imposta un valore che determina se premiscelare o meno le immagini trasparenti con il colore di sfondo nero. |
| [PreserveFormFields](../../aspose.words.saving/pdfsaveoptions/preserveformfields/) { get; set; } | Specifica se conservare i campi del modulo di Microsoft Word come campi del modulo in PDF o convertirli in testo. Il valore predefinito è`falso` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formatta bene l'output dove applicabile. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Viene chiamato durante il salvataggio di un documento e accetta dati sullo stato di avanzamento del salvataggio. |
| [RenderChoiceFormFieldBorder](../../aspose.words.saving/pdfsaveoptions/renderchoiceformfieldborder/) { get; set; } | Specifica se visualizzare il bordo del campo del modulo di scelta PDF. |
| override [SaveFormat](../../aspose.words.saving/pdfsaveoptions/saveformat/) { get; set; } | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere soloPdf . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è`null` e non vengono utilizzati file temporanei. |
| [TextCompression](../../aspose.words.saving/pdfsaveoptions/textcompression/) { get; set; } | Specifica il tipo di compressione da utilizzare per tutto il contenuto testuale nel documento. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determina se gli attributi del font verranno modificati in base al codice carattere utilizzato. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è`falso` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è`VERO` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/pdfsaveoptions/usebookfoldprintingsettings/) { get; set; } | Ottiene o imposta un valore booleano che indica se il documento deve essere salvato utilizzando un layout di stampa opuscolo, se specificato tramite[`MultiplePages`](../../aspose.words/pagesetup/multiplepages/) . |
| [UseCoreFonts](../../aspose.words.saving/pdfsaveoptions/usecorefonts/) { get; set; } | Ottiene o imposta un valore che determina se sostituire o meno i font TrueType Arial, Times New Roman, Courier New e Symbol con i font PDF Type 1 principali. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (ad esempio lenti). |
| [UseSdtTagAsFormFieldName](../../aspose.words.saving/pdfsaveoptions/usesdttagasformfieldname/) { get; set; } | Specifica se utilizzare il controllo SDT Tag o la proprietà Id come nome del campo modulo in PDF. |
| [ZoomBehavior](../../aspose.words.saving/pdfsaveoptions/zoombehavior/) { get; set; } | Ottiene o imposta un valore che determina quale tipo di zoom deve essere applicato quando un documento viene aperto con un visualizzatore PDF. |
| [ZoomFactor](../../aspose.words.saving/pdfsaveoptions/zoomfactor/) { get; set; } | Ottiene o imposta un valore che determina il fattore di zoom (in percentuale) per un documento. |

## Metodi

| Nome | Descrizione |
| --- | --- |
| [Clone](../../aspose.words.saving/pdfsaveoptions/clone/)() | Crea un clone profondo di questo oggetto. |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals/)(*object*) | Determina se l'oggetto specificato ha un valore uguale all'oggetto corrente. |

## Esempi

Mostra come modificare il colore dell'immagine con la proprietà delle opzioni di salvataggio.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
// Impostare la proprietà "ColorMode" su "Grayscale" per visualizzare tutte le immagini del documento in bianco e nero.
// Con questa impostazione la dimensione del documento di output potrebbe essere maggiore.
// Impostare la proprietà "ColorMode" su "Normale" per visualizzare tutte le immagini a colori.
PdfSaveOptions pdfSaveOptions = new PdfSaveOptions { ColorMode = colorMode };

doc.Save(ArtifactsDir + "PdfSaveOptions.ColorRendering.pdf", pdfSaveOptions);
```

Mostra come applicare la compressione del testo quando si salva un documento in formato PDF.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

for (int i = 0; i < 100; i++)
    builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                    "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Imposta la proprietà "TextCompression" su "PdfTextCompression.None" per non applicare alcun
// compressione del testo quando salviamo il documento in PDF.
// Imposta la proprietà "TextCompression" su "PdfTextCompression.Flate" per applicare la compressione ZIP
// in testo quando salviamo il documento in PDF. Più grande è il documento, maggiore sarà l'impatto.
options.TextCompression = pdfTextCompression;

doc.Save(ArtifactsDir + "PdfSaveOptions.TextCompression.pdf", options);
```

Mostra come convertire un intero documento in PDF con tre livelli nella struttura del documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserire le intestazioni dei livelli da 1 a 5.
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

// Creiamo un oggetto "PdfSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .PDF.
PdfSaveOptions options = new PdfSaveOptions();

// Il documento PDF di output conterrà una struttura, ovvero un indice che elenca le intestazioni nel corpo del documento.
// Cliccando su una voce in questo schema verremo indirizzati alla posizione della rispettiva intestazione.
// Impostare la proprietà "HeadingsOutlineLevels" su "4" per escludere dalla struttura tutte le intestazioni i cui livelli sono superiori a 4.
options.OutlineOptions.HeadingsOutlineLevels = 4;

// Se una voce di struttura ha voci successive di livello superiore tra sé stessa e la voce successiva dello stesso livello o di livello inferiore,
// apparirà una freccia a sinistra della voce. Questa voce è la "proprietaria" di diverse "sotto-voci" di questo tipo.
// Nel nostro documento, le voci di struttura del 5° livello di intestazione sono sottovoci della seconda voce di struttura del 4° livello,
// le voci di 4° e 5° livello di intestazione sono sottovoci della seconda voce di 3° livello, e così via.
// Nella struttura, possiamo cliccare sulla freccia della voce "proprietario" per comprimere/espandere tutte le sue sotto-voci.
// Imposta la proprietà "ExpandedOutlineLevels" su "2" per espandere automaticamente tutte le voci di struttura di livello 2 e inferiore dell'intestazione
// e comprimere tutte le voci di livello 3 e superiori quando apriamo il documento.
options.OutlineOptions.ExpandedOutlineLevels = 2;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExpandedOutlineLevels.pdf", options);
```

### Guarda anche

* class [FixedPageSaveOptions](../fixedpagesaveoptions/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
