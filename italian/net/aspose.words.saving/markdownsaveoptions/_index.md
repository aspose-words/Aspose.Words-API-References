---
title: Class MarkdownSaveOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.MarkdownSaveOptions classe. Classe per specificare opzioni aggiuntive durante il salvataggio di un documento inMarkdown formato.
type: docs
weight: 5000
url: /it/net/aspose.words.saving/markdownsaveoptions/
---
## MarkdownSaveOptions class

Classe per specificare opzioni aggiuntive durante il salvataggio di un documento inMarkdown formato.

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
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di caratteri con contorni PostScript quando l'incorporamento di caratteri TrueType in un documento viene salvato. Il valore predefinito è **falso** . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso del modello predefinito (incluso il nome file). Il valore predefinito per questa proprietà è **stringa vuota** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering delle forme DrawingML. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Specifica la codifica da utilizzare durante l'esportazione nei formati di testo. Il valore predefinito è **Codifica.UTF8** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Se true, fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è **VERO** . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Specifica il modo in cui le intestazioni e i piè di pagina vengono esportati nei formati di testo. Il valore predefinito èPrimaryOnly . |
| [ExportImagesAsBase64](../../aspose.words.saving/markdownsaveoptions/exportimagesasbase64/) { get; set; } | Specifica se le immagini vengono salvate nel formato Base64 nel file di output. L'impostazione predefinita è`falso` . |
| [FlatOpcXmlMappingOnly](../../aspose.words.saving/saveoptions/flatopcxmlmappingonly/) { get; set; } | Ottiene o imposta un valore che determina i formati di documento in base ai quali è consentito mappare[`XmlMapping`](../../aspose.words.markup/structureddocumenttag/xmlmapping/) . Solo per impostazione predefinitaFlatOpc il formato del documento può essere mappato. |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Consente di specificare se le interruzioni di pagina devono essere conservate durante l'esportazione. |
| [ImageSavingCallback](../../aspose.words.saving/markdownsaveoptions/imagesavingcallback/) { get; set; } | Consente di controllare come vengono salvate le immagini quando un documento viene salvato in Markdown formato. |
| [ImagesFolder](../../aspose.words.saving/markdownsaveoptions/imagesfolder/) { get; set; } | Specifica la cartella fisica in cui vengono salvate le immagini durante l'esportazione di un documento in Markdown formato. L'impostazione predefinita è una stringa vuota. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina la modalità di rendering degli oggetti Ink (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se eseguire l'ottimizzazione della memoria prima di salvare il documento. Il valore predefinito per questa proprietà è **falso** . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Specifica la stringa da utilizzare come interruzione di paragrafo durante l'esportazione nei formati di testo. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formati graziosi di output ove applicabile. Il valore predefinito è **falso** . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Chiamato durante il salvataggio di un documento e accetta i dati sull'avanzamento del salvataggio. |
| override [SaveFormat](../../aspose.words.saving/markdownsaveoptions/saveformat/) { get; set; } | Specifica il formato in cui verrà salvato il documento se viene utilizzato questo oggetto opzioni di salvataggio. Può essereMarkdown . |
| [TableContentAlignment](../../aspose.words.saving/markdownsaveoptions/tablecontentalignment/) { get; set; } | Ottiene o imposta un valore che specifica come allineare i contenuti nelle tabelle durante l'esportazione inMarkdown format. Il valore predefinito èAuto . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzata durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita questa proprietà è`nullo` e non vengono utilizzati file temporanei. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è false; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è **VERO** . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateSdtContent](../../aspose.words.saving/saveoptions/updatesdtcontent/) { get; set; } | Ottiene o imposta il valore che determina se il contenuto di[`StructuredDocumentTag`](../../aspose.words.markup/structureddocumenttag/) viene aggiornato prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-alias per il rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (cioè lenti). |

### Guarda anche

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


