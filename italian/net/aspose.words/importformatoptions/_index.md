---
title: ImportFormatOptions Class
linktitle: ImportFormatOptions
articleTitle: ImportFormatOptions
second_title: Aspose.Words per .NET
description: Scopri Aspose.Words.ImportFormatOptions per personalizzare la formattazione dei documenti. Migliora il tuo output con impostazioni di importazione personalizzate per risultati ottimali.
type: docs
weight: 3690
url: /it/net/aspose.words/importformatoptions/
---
## ImportFormatOptions class

Consente di specificare varie opzioni di importazione per formattare l'output.

Per saperne di più, visita il[Specificare le opzioni di carico](https://docs.aspose.com/words/net/specify-load-options/) articolo di documentazione.

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
| [AdjustSentenceAndWordSpacing](../../aspose.words/importformatoptions/adjustsentenceandwordspacing/) { get; set; } | Ottiene o imposta un valore booleano che specifica se regolare automaticamente la spaziatura delle frasi e delle parole. Il valore predefinito è`falso` . |
| [ForceCopyStyles](../../aspose.words/importformatoptions/forcecopystyles/) { get; set; } | Ottiene o imposta un valore booleano che indica di copiare gli stili in conflitto inKeepSourceFormatting mode. Il valore predefinito è`falso` . |
| [IgnoreHeaderFooter](../../aspose.words/importformatoptions/ignoreheaderfooter/) { get; set; } | Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto delle intestazioni/piè di pagina viene ignorata seKeepSourceFormatting viene utilizzata la modalità. Il valore predefinito è`VERO` . |
| [IgnoreTextBoxes](../../aspose.words/importformatoptions/ignoretextboxes/) { get; set; } | Ottiene o imposta un valore booleano che specifica che la formattazione di origine del contenuto delle caselle di testo viene ignorata seKeepSourceFormatting viene utilizzata la modalità. Il valore predefinito è`VERO` . |
| [KeepSourceNumbering](../../aspose.words/importformatoptions/keepsourcenumbering/) { get; set; } | Ottiene o imposta un valore booleano che specifica come verrà importata la numerazione quando si verifica un conflitto nei documenti di origine e di destinazione. Il valore predefinito è`falso` . |
| [MergePastedLists](../../aspose.words/importformatoptions/mergepastedlists/) { get; set; } | Ottiene o imposta un valore booleano che specifica se gli elenchi incollati verranno uniti agli elenchi circostanti. Il valore predefinito è`falso` . |
| [SmartStyleBehavior](../../aspose.words/importformatoptions/smartstylebehavior/) { get; set; } | Ottiene o imposta un valore booleano che specifica come verranno importati gli stili quando hanno nomi uguali nei documenti di origine e di destinazione. Il valore predefinito è`falso` . |

## Esempi

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

// Clona il documento e modifica lo stile "MyStyle" del clone, in modo che abbia un colore diverso da quello dell'originale.
// Se inseriamo il clone nel documento originale, i due stili con lo stesso nome causeranno un conflitto.
Document srcDoc = dstDoc.Clone();
srcDoc.Styles["MyStyle"].Font.Color = Color.Red;

// Quando abilitiamo SmartStyleBehavior e utilizziamo la modalità di formato di importazione KeepSourceFormatting,
// Aspose.Words risolverà i conflitti di stile convertendo gli stili del documento sorgente.
// con gli stessi nomi degli stili di destinazione in attributi di paragrafo diretti.
ImportFormatOptions options = new ImportFormatOptions();
options.SmartStyleBehavior = true;

builder.InsertDocument(srcDoc, ImportFormatMode.KeepSourceFormatting, options);

dstDoc.Save(ArtifactsDir + "DocumentBuilder.SmartStyleBehavior.docx");
```

### Guarda anche

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)
