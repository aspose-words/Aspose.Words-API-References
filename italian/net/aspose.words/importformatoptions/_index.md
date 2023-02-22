---
title: Class ImportFormatOptions
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.ImportFormatOptions classe. Consente di specificare varie opzioni di importazione per formattare loutput.
type: docs
weight: 3040
url: /it/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Consente di specificare varie opzioni di importazione per formattare l'output.

```csharp
public class ImportFormatOptions
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [ImportFormatOptions](importformatoptions/)() | Default_Costruttore |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Ottiene o imposta un valore booleano che indica di copiare gli stili in conflitto inKeepSourceFormatting mode. Il valore predefinito è`falso` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Ottiene o imposta un valore booleano che specifica la formattazione di origine del contenuto di intestazioni/piè di pagina ignorata seKeepSourceFormatting viene utilizzata la modalità. Il valore predefinito è`VERO` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Ottiene o imposta un valore booleano che specifica la formattazione di origine del contenuto delle caselle di testo ignorata seKeepSourceFormatting viene utilizzata la modalità. Il valore predefinito è`VERO` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Ottiene o imposta un valore booleano che specifica come verrà importata la numerazione quando si verifica un conflitto nei documenti di origine e di destinazione. Il valore predefinito è`falso` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Ottiene o imposta un valore booleano che specifica se gli elenchi incollati verranno uniti agli elenchi circostanti. Il valore predefinito è`falso` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Ottiene o imposta un valore booleano che specifica come verranno importati gli stili quando hanno nomi uguali nei documenti di origine e di destinazione. Il valore predefinito è`falso` . |

### Esempi

Mostra come risolvere gli stili duplicati durante l'inserimento di documenti.

```csharp
Document dstDoc = new Document();
DocumentBuilder builder = new DocumentBuilder(dstDoc);

Style myStyle = builder.Document.Styles.Add(StyleType.Paragraph, "MyStyle");
myStyle.Font.Size = 14;
myStyle.Font.Name = "Courier New";
myStyle.Font.Color = Color.Blue;

builder.ParagraphFormat.StyleName = myStyle.Name;
builder.Writeln("Hello world!");

// Clona il documento e modifica lo stile "MyStyle" del clone, quindi è di un colore diverso da quello dell'originale.
// Se inseriamo il clone nel documento originale, i due stili con lo stesso nome causeranno uno scontro.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Quando abilitiamo SmartStyleBehavior e utilizziamo la modalità di formato di importazione KeepSourceFormatting,
// Aspose.Words risolverà i conflitti di stile convertendo gli stili del documento sorgente.
// con gli stessi nomi degli stili di destinazione negli attributi di paragrafo diretto.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


