---
title: DocSaveOptions Class
linktitle: DocSaveOptions
articleTitle: DocSaveOptions
second_title: Aspose.Words per .NET
description: Ottimizza il salvataggio dei documenti con Aspose.Words.Saving.DocSaveOptions. Personalizza i tuoi formati Doc e Dot per una maggiore qualità e flessibilità.
type: docs
weight: 5680
url: /it/net/aspose.words.saving/docsaveoptions/
---
## DocSaveOptions class

Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento inDoc oppure Dot formato.

Per saperne di più, visita il[Specificare le opzioni di salvataggio](https://docs.aspose.com/words/net/specify-save-options/) articolo di documentazione.

```csharp
public class DocSaveOptions : SaveOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [DocSaveOptions](docsaveoptions/#constructor)() | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nelDoc formato. |
| [DocSaveOptions](docsaveoptions/#constructor_1)(*[SaveFormat](../../aspose.words/saveformat/)*) | Inizializza una nuova istanza di questa classe che può essere utilizzata per salvare un documento nelDoc oppure Dot formato. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è`falso` . |
| [AlwaysCompressMetafiles](../../aspose.words.saving/docsaveoptions/alwayscompressmetafiles/) { get; set; } | Quando`falso` , i metafile di piccole dimensioni non vengono compressi per motivi di prestazioni. Il valore predefinito è`VERO` , tutti i metafile vengono compressi indipendentemente dalla loro dimensione. |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso al modello predefinito (incluso il nome del file). Il valore predefinito per questa proprietà è**stringa vuota** (Empty ). |
| [DigitalSignatureDetails](../../aspose.words.saving/docsaveoptions/digitalsignaturedetails/) { get; set; } | Ottiene o imposta[`DigitalSignatureDetails`](../digitalsignaturedetails/) oggetto utilizzato per firmare un documento. |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quando`VERO` , fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è`VERO` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti ink (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è`falso` . |
| [Password](../../aspose.words.saving/docsaveoptions/password/) { get; set; } | Ottiene/imposta una password per crittografare il documento utilizzando il metodo di crittografia RC4. |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formatta bene l'output dove applicabile. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Viene chiamato durante il salvataggio di un documento e accetta dati sullo stato di avanzamento del salvataggio. |
| override [SaveFormat](../../aspose.words.saving/docsaveoptions/saveformat/) { get; set; } | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essereDoc ODot . |
| [SavePictureBullet](../../aspose.words.saving/docsaveoptions/savepicturebullet/) { get; set; } | Quando`falso` , i dati PictureBullet non vengono salvati nel documento di output. Il valore predefinito è`VERO` . |
| [SaveRoutingSlip](../../aspose.words.saving/docsaveoptions/saveroutingslip/) { get; set; } | Quando`falso` , i dati RoutingSlip non vengono salvati nel documento di output. Il valore predefinito è`VERO` . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è`null` e non vengono utilizzati file temporanei. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determina se gli attributi del font verranno modificati in base al codice carattere utilizzato. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è`falso` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è`VERO` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (ad esempio lenti). |

## Osservazioni

Al momento fornisce solo il[`SaveFormat`](./saveformat/) proprietà, ma in futuro saranno aggiunte altre opzioni, come una password di crittografia o impostazioni di firma digitale.

## Esempi

Mostra come impostare le opzioni di salvataggio per i vecchi formati di Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

DocSaveOptions options = new DocSaveOptions(SaveFormat.Doc);

// Imposta una password che proteggerà il caricamento del documento da parte di Microsoft Word o Aspose.Words.
// Nota che questo non crittografa in alcun modo il contenuto del documento.
options.Password = "MyPassword";

// Se il documento contiene una bolla di accompagnamento, possiamo conservarla durante il salvataggio impostando questo flag su true.
options.SaveRoutingSlip = true;

doc.Save(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", options);

// Per poter caricare il documento,
// dovremo applicare la password specificata nell'oggetto DocSaveOptions in un oggetto LoadOptions.
Assert.Throws<IncorrectPasswordException>(() => doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc"));

LoadOptions loadOptions = new LoadOptions("MyPassword");
doc = new Document(ArtifactsDir + "DocSaveOptions.SaveAsDoc.doc", loadOptions);

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Guarda anche

* class [SaveOptions](../saveoptions/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
