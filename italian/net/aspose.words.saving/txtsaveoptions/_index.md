---
title: TxtSaveOptions Class
linktitle: TxtSaveOptions
articleTitle: TxtSaveOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.TxtSaveOptions per un salvataggio documenti migliorato. Personalizza il formato del testo con potenti opzioni per risultati ottimali.
type: docs
weight: 6460
url: /it/net/aspose.words.saving/txtsaveoptions/
---
## TxtSaveOptions class

Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento inText formato.

Per saperne di più, visita il[Specificare le opzioni di salvataggio](https://docs.aspose.com/words/net/specify-save-options/) articolo di documentazione.

```csharp
public class TxtSaveOptions : TxtSaveOptionsBase
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [TxtSaveOptions](txtsaveoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AddBidiMarks](../../aspose.words.saving/txtsaveoptions/addbidimarks/) { get; set; } | Specifica se aggiungere marcatori bidirezionali prima di ogni esecuzione BiDi durante l'esportazione in formato di testo normale. |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è`falso` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso al modello predefinito (incluso il nome del file). Il valore predefinito per questa proprietà è**stringa vuota** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [Encoding](../../aspose.words.saving/txtsaveoptionsbase/encoding/) { get; set; } | Specifica la codifica da utilizzare durante l'esportazione in formati di testo. Il valore predefinito è **Codifica.UTF8** . |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quando`VERO` , fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è`VERO` . |
| [ExportHeadersFootersMode](../../aspose.words.saving/txtsaveoptionsbase/exportheadersfootersmode/) { get; set; } | Specifica il modo in cui le intestazioni e i piè di pagina vengono esportati nei formati di testo. Il valore predefinito èPrimaryOnly . |
| [ForcePageBreaks](../../aspose.words.saving/txtsaveoptionsbase/forcepagebreaks/) { get; set; } | Consente di specificare se le interruzioni di pagina devono essere mantenute durante l'esportazione. |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti ink (InkML). |
| [ListIndentation](../../aspose.words.saving/txtsaveoptions/listindentation/) { get; } | Ottiene un[`TxtListIndentation`](../txtlistindentation/)oggetto che specifica quanti e quali caratteri utilizzare per l'indentazione dei livelli di elenco. Per impostazione predefinita, il conteggio del carattere '\0' è zero, il che significa nessuna indentazione. |
| [MaxCharactersPerLine](../../aspose.words.saving/txtsaveoptions/maxcharactersperline/) { get; set; } | Ottiene o imposta un valore intero che specifica il numero massimo di caratteri per riga. Il valore predefinito è 0, ovvero nessun limite. |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è`falso` . |
| [ParagraphBreak](../../aspose.words.saving/txtsaveoptionsbase/paragraphbreak/) { get; set; } | Specifica la stringa da utilizzare come interruzione di paragrafo durante l'esportazione in formati di testo. |
| [PreserveTableLayout](../../aspose.words.saving/txtsaveoptions/preservetablelayout/) { get; set; } | Specifica se il programma deve tentare di preservare il layout delle tabelle durante il salvataggio nel formato di testo normale. Il valore predefinito è`falso` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formatta bene l'output dove applicabile. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Viene chiamato durante il salvataggio di un documento e accetta dati sullo stato di avanzamento del salvataggio. |
| override [SaveFormat](../../aspose.words.saving/txtsaveoptions/saveformat/) { get; set; } | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere soloText . |
| [SimplifyListLabels](../../aspose.words.saving/txtsaveoptions/simplifylistlabels/) { get; set; } | Specifica se il programma deve semplificare le etichette degli elenchi nel caso in cui la formattazione complessa delle etichette non venga rappresentata adeguatamente dal testo normale. |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è`null` e non vengono utilizzati file temporanei. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determina se gli attributi del font verranno modificati in base al codice carattere utilizzato. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è`falso` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è`VERO` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (ad esempio lenti). |

## Esempi

Mostra come salvare un documento .txt con un'interruzione di paragrafo personalizzata.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Paragraph 1.");
builder.Writeln("Paragraph 2.");
builder.Write("Paragraph 3.");

// Creiamo un oggetto "TxtSaveOptions", che possiamo passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento in testo normale.
TxtSaveOptions txtSaveOptions = new TxtSaveOptions();

Assert.AreEqual(SaveFormat.Text, txtSaveOptions.SaveFormat);

// Imposta "ParagraphBreak" su un valore personalizzato che desideriamo inserire alla fine di ogni paragrafo.
txtSaveOptions.ParagraphBreak = " End of paragraph.\n\n\t";

doc.Save(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt", txtSaveOptions);

string docText = File.ReadAllText(ArtifactsDir + "TxtSaveOptions.ParagraphBreak.txt");

Assert.AreEqual("Paragraph 1. End of paragraph.\n\n\t" +
                "Paragraph 2. End of paragraph.\n\n\t" +
                "Paragraph 3. End of paragraph.\n\n\t", docText);
```

### Guarda anche

* class [TxtSaveOptionsBase](../txtsaveoptionsbase/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
