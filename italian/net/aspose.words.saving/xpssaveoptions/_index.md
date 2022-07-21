---
title: XpsSaveOptions
second_title: Aspose.Words per .NET API Reference
description: Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento nel fileXps formato.
type: docs
weight: 5430
url: /it/net/aspose.words.saving/xpssaveoptions/
---
## XpsSaveOptions class

Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento nel fileXps formato.

```csharp
public class XpsSaveOptions : FixedPageSaveOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [XpsSaveOptions](xpssaveoptions#constructor)() | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nelXps formato. |
| [XpsSaveOptions](xpssaveoptions#constructor_1)(SaveFormat) | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nelXps oOpenXps formato. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di caratteri con contorni PostScript quando l'incorporamento di caratteri TrueType in un documento viene salvato. Il valore predefinito è **falso** . |
| [ColorMode](../../aspose.words.saving/fixedpagesaveoptions/colormode) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering dei colori. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate) { get; set; } | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **stringa vuota** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering delle forme DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname) { get; set; } | Se true, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **VERO** . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly) { get; set; } | Ottiene o imposta un valore che determina i formati di documento in base ai quali è consentito mappare[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping) . Solo per impostazione predefinitaFlatOpc il formato del documento può essere mappato. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli oggetti Ink (InkML). |
| [JpegQuality](../../aspose.words.saving/fixedpagesaveoptions/jpegquality) { get; set; } | Ottiene o imposta un valore che determina la qualità delle immagini JPEG all'interno del documento Html. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization) { get; set; } | Ottiene o imposta il valore che determina se eseguire l'ottimizzazione della memoria prima di salvare il documento. Il valore predefinito per questa proprietà è **falso** . |
| [MetafileRenderingOptions](../../aspose.words.saving/fixedpagesaveoptions/metafilerenderingoptions) { get; set; } | Consente di specificare le opzioni di rendering del metafile. |
| [NumeralFormat](../../aspose.words.saving/fixedpagesaveoptions/numeralformat) { get; set; } | Ottiene o imposta[`NumeralFormat`](../numeralformat) utilizzato per il rendering dei numeri. I numeri europei vengono utilizzati per impostazione predefinita. |
| virtual [OptimizeOutput](../../aspose.words.saving/fixedpagesaveoptions/optimizeoutput) { get; set; } | Il flag indica se è necessario ottimizzare l'output. Se questo flag è impostato, le tele nidificate ridondanti e le tele vuote vengono rimosse, anche i glifi vicini con la stessa formattazione vengono concatenati. Nota: la precisione della visualizzazione del contenuto potrebbe essere compromessa se questa proprietà è impostata su true. L'impostazione predefinita è false. |
| [OutlineOptions](../../aspose.words.saving/xpssaveoptions/outlineoptions) { get; } | Consente di specificare le opzioni del contorno. |
| [PageSavingCallback](../../aspose.words.saving/fixedpagesaveoptions/pagesavingcallback) { get; set; } | Consente di controllare come vengono salvate le pagine separate quando un documento viene esportato in un formato pagina fisso. |
| [PageSet](../../aspose.words.saving/fixedpagesaveoptions/pageset) { get; set; } | Ottiene o imposta le pagine di cui eseguire il rendering. Il valore predefinito è tutte le pagine nel documento. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat) { get; set; } | Quando`VERO` , formati graziosi di output ove applicabile. Il valore predefinito è **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback) { get; set; } | Chiamato durante il salvataggio di un documento e accetta i dati sull'avanzamento del salvataggio. |
| override [SaveFormat](../../aspose.words.saving/xpssaveoptions/saveformat) { get; set; } | Specifica il formato in cui verrà salvato il documento se viene utilizzato questo oggetto opzioni di salvataggio. Può essereXps . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder) { get; set; } | Specifica la cartella per i file temporanei utilizzata durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è **VERO** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent) { get; set; } | Ottiene o imposta il valore che determina se il contenuto di[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag) viene aggiornato prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-alias per il rendering. |
| [UseBookFoldPrintingSettings](../../aspose.words.saving/xpssaveoptions/usebookfoldprintingsettings) { get; set; } | Ottiene o imposta un valore booleano che indica se il documento deve essere salvato utilizzando un layout di stampa opuscolo, se specificato tramite[`MultiplePages`](../../aspose.words/pagesetup/multiplepages) . |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (cioè lenti). |

## Metodi

| Nome | Descrizione |
| --- | --- |
| override [Equals](../../aspose.words.saving/fixedpagesaveoptions/equals)(object) | Determina se l'oggetto specificato è uguale in valore all'oggetto corrente. |

### Esempi

Mostra come limitare il livello delle intestazioni che appariranno nella struttura di un documento XPS salvato.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Inserisce intestazioni che possono fungere da voci TOC di livello 1, 2 e poi 3.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;

Assert.True(builder.ParagraphFormat.IsHeading);

builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;

builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;

builder.Writeln("Heading 1.2.1");
builder.Writeln("Heading 1.2.2");

// Crea un oggetto "XpsSaveOptions" che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui quel metodo converte il documento in .XPS.
XpsSaveOptions saveOptions = new XpsSaveOptions();

Assert.AreEqual(SaveFormat.Xps, saveOptions.SaveFormat);

// Il documento XPS di output conterrà uno schema, un sommario che elenca i titoli nel corpo del documento.
// Cliccando su una voce in questo schema ci porterà alla posizione della rispettiva intestazione.
// Imposta la proprietà "HeadingsOutlineLevels" su "2" per escludere tutte le intestazioni i cui livelli sono superiori a 2 dalla struttura.
// Le ultime due intestazioni che abbiamo inserito sopra non appariranno.
saveOptions.OutlineOptions.HeadingsOutlineLevels = 2;

doc.Save(ArtifactsDir + "XpsSaveOptions.OutlineLevels.xps", saveOptions);
```

### Guarda anche

* class [FixedPageSaveOptions](../fixedpagesaveoptions)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving)
* assemblea [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
