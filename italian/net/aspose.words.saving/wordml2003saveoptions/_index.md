---
title: WordML2003SaveOptions Class
linktitle: WordML2003SaveOptions
articleTitle: WordML2003SaveOptions
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.WordML2003SaveOptions per migliorare l'esperienza di salvataggio dei documenti in formato WordML con opzioni personalizzabili.
type: docs
weight: 6480
url: /it/net/aspose.words.saving/wordml2003saveoptions/
---
## WordML2003SaveOptions class

Può essere utilizzato per specificare opzioni aggiuntive durante il salvataggio di un documento inWordML formato.

Per saperne di più, visita il[Specificare le opzioni di salvataggio](https://docs.aspose.com/words/net/specify-save-options/) articolo di documentazione.

```csharp
public class WordML2003SaveOptions : SaveOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [WordML2003SaveOptions](wordml2003saveoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [AllowEmbeddingPostScriptFonts](../../aspose.words.saving/saveoptions/allowembeddingpostscriptfonts/) { get; set; } | Ottiene o imposta un valore booleano che indica se consentire l'incorporamento di font con contorni PostScript quando si incorporano font TrueType in un documento al momento del salvataggio. Il valore predefinito è`falso` . |
| [CustomTimeZoneInfo](../../aspose.words.saving/saveoptions/customtimezoneinfo/) { get; set; } | Ottiene o imposta il fuso orario locale personalizzato utilizzato per i campi data/ora. |
| [DefaultTemplate](../../aspose.words.saving/saveoptions/defaulttemplate/) { get; set; } | Ottiene o imposta il percorso al modello predefinito (incluso il nome del file). Il valore predefinito per questa proprietà è**stringa vuota** (Empty ). |
| [Dml3DEffectsRenderingMode](../../aspose.words.saving/saveoptions/dml3deffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti 3D. |
| virtual [DmlEffectsRenderingMode](../../aspose.words.saving/saveoptions/dmleffectsrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli effetti DrawingML. |
| [DmlRenderingMode](../../aspose.words.saving/saveoptions/dmlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzate le forme DrawingML. |
| [ExportGeneratorName](../../aspose.words.saving/saveoptions/exportgeneratorname/) { get; set; } | Quando`VERO` , fa sì che il nome e la versione di Aspose.Words vengano incorporati nei file prodotti. Il valore predefinito è`VERO` . |
| [ImlRenderingMode](../../aspose.words.saving/saveoptions/imlrenderingmode/) { get; set; } | Ottiene o imposta un valore che determina come vengono renderizzati gli oggetti ink (InkML). |
| [MemoryOptimization](../../aspose.words.saving/saveoptions/memoryoptimization/) { get; set; } | Ottiene o imposta il valore che determina se l'ottimizzazione della memoria deve essere eseguita prima di salvare il documento. Il valore predefinito per questa proprietà è`falso` . |
| [PrettyFormat](../../aspose.words.saving/saveoptions/prettyformat/) { get; set; } | Quando`VERO` , formatta bene l'output dove applicabile. Il valore predefinito è`falso` . |
| [ProgressCallback](../../aspose.words.saving/saveoptions/progresscallback/) { get; set; } | Viene chiamato durante il salvataggio di un documento e accetta dati sullo stato di avanzamento del salvataggio. |
| override [SaveFormat](../../aspose.words.saving/wordml2003saveoptions/saveformat/) { get; set; } | Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essere soloWordML . |
| [TempFolder](../../aspose.words.saving/saveoptions/tempfolder/) { get; set; } | Specifica la cartella per i file temporanei utilizzati durante il salvataggio in un file DOC o DOCX. Per impostazione predefinita, questa proprietà è`null` e non vengono utilizzati file temporanei. |
| [UpdateAmbiguousTextFont](../../aspose.words.saving/saveoptions/updateambiguoustextfont/) { get; set; } | Determina se gli attributi del font verranno modificati in base al codice carattere utilizzato. |
| [UpdateCreatedTimeProperty](../../aspose.words.saving/saveoptions/updatecreatedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`CreatedTime`](../../aspose.words.properties/builtindocumentproperties/createdtime/) la proprietà viene aggiornata prima del salvataggio. Il valore predefinito è`falso` ; |
| [UpdateFields](../../aspose.words.saving/saveoptions/updatefields/) { get; set; } | Ottiene o imposta un valore che determina se i campi di determinati tipi devono essere aggiornati prima di salvare il documento in un formato di pagina fisso. Il valore predefinito per questa proprietà è`VERO` . |
| [UpdateLastPrintedProperty](../../aspose.words.saving/saveoptions/updatelastprintedproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastPrinted`](../../aspose.words.properties/builtindocumentproperties/lastprinted/) la proprietà viene aggiornata prima del salvataggio. |
| [UpdateLastSavedTimeProperty](../../aspose.words.saving/saveoptions/updatelastsavedtimeproperty/) { get; set; } | Ottiene o imposta un valore che determina se il[`LastSavedTime`](../../aspose.words.properties/builtindocumentproperties/lastsavedtime/) la proprietà viene aggiornata prima del salvataggio. |
| [UseAntiAliasing](../../aspose.words.saving/saveoptions/useantialiasing/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno l'anti-aliasing per il rendering. |
| [UseHighQualityRendering](../../aspose.words.saving/saveoptions/usehighqualityrendering/) { get; set; } | Ottiene o imposta un valore che determina se utilizzare o meno algoritmi di rendering di alta qualità (ad esempio lenti). |

## Osservazioni

Al momento fornisce solo il[`SaveFormat`](./saveformat/) proprietà, ma in futuro potrebbero essere aggiunte altre opzioni.

## Esempi

Mostra come gestire l'ottimizzazione della memoria.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea un oggetto "WordML2003SaveOptions" da passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento nel formato di salvataggio WordML.
WordML2003SaveOptions options = new WordML2003SaveOptions();

// Imposta il flag "MemoryOptimization" su "true" per ridurre il consumo di memoria
// durante l'operazione di salvataggio del documento, a scapito di un tempo di salvataggio più lungo.
// Impostare il flag "MemoryOptimization" su "false" per salvare il documento normalmente.
options.MemoryOptimization = memoryOptimization;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.MemoryOptimization.xml", options);
```

Mostra come gestire il contenuto grezzo del documento di output.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Crea un oggetto "WordML2003SaveOptions" da passare al metodo "Save" del documento
// per modificare il modo in cui salviamo il documento nel formato di salvataggio WordML.
WordML2003SaveOptions options = new WordML2003SaveOptions();

Assert.AreEqual(SaveFormat.WordML, options.SaveFormat);

// Imposta la proprietà "PrettyFormat" su "true" per applicare l'indentazione del carattere di tabulazione e
// nuove righe per rendere più facile la lettura del contenuto grezzo del documento di output.
// Impostare la proprietà "PrettyFormat" su "false" per salvare il contenuto grezzo del documento in un corpo di testo continuo.
options.PrettyFormat = prettyFormat;

doc.Save(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml", options);

string fileContents = File.ReadAllText(ArtifactsDir + "WordML2003SaveOptions.PrettyFormat.xml");
string newLine = Environment.NewLine;

if (prettyFormat)
    Assert.True(fileContents.Contains(
        $"<o:DocumentProperties>{newLine}\t\t" +
            $"<o:Revision>1</o:Revision>{newLine}\t\t" +
            $"<o:TotalTime>0</o:TotalTime>{newLine}\t\t" +
            $"<o:Pages>1</o:Pages>{newLine}\t\t" +
            $"<o:Words>0</o:Words>{newLine}\t\t" +
            $"<o:Characters>0</o:Characters>{newLine}\t\t" +
            $"<o:Lines>1</o:Lines>{newLine}\t\t" +
            $"<o:Paragraphs>1</o:Paragraphs>{newLine}\t\t" +
            $"<o:CharactersWithSpaces>0</o:CharactersWithSpaces>{newLine}\t\t" +
            $"<o:Version>11.5606</o:Version>{newLine}\t" +
        "</o:DocumentProperties>"));
else
    Assert.True(fileContents.Contains(
        "<o:DocumentProperties><o:Revision>1</o:Revision><o:TotalTime>0</o:TotalTime><o:Pages>1</o:Pages>" +
        "<o:Words>0</o:Words><o:Characters>0</o:Characters><o:Lines>1</o:Lines><o:Paragraphs>1</o:Paragraphs>" +
        "<o:CharactersWithSpaces>0</o:CharactersWithSpaces><o:Version>11.5606</o:Version></o:DocumentProperties>"));
```

### Guarda anche

* class [SaveOptions](../saveoptions/)
* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
