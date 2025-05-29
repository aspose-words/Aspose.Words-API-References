---
title: ImportFormatOptions.SmartStyleBehavior
linktitle: SmartStyleBehavior
articleTitle: SmartStyleBehavior
second_title: Aspose.Words per .NET
description: Scopri come la proprietà SmartStyleBehavior di ImportFormatOptions ottimizza l'importazione di stili con nomi uguali nei documenti. Personalizza il tuo processo di importazione senza sforzo!
type: docs
weight: 80
url: /it/net/aspose.words/importformatoptions/smartstylebehavior/
---
## ImportFormatOptions.SmartStyleBehavior property

Ottiene o imposta un valore booleano che specifica come verranno importati gli stili quando hanno nomi uguali nei documenti di origine e di destinazione. Il valore predefinito è`falso` .

```csharp
public bool SmartStyleBehavior { get; set; }
```

## Osservazioni

Quando questa opzione è**abilitato** , lo stile sorgente verrà espanso in attributi diretti all'interno del documento di destinazione a , seKeepSourceFormatting viene utilizzata la modalità di importazione.

Quando questa opzione è**disabile**, lo stile sorgente verrà espanso solo se numerato. Gli attributi di destinazione Exist non verranno sovrascritti, inclusi gli elenchi.

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

* class [ImportFormatOptions](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
