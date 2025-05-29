---
title: DocSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words per .NET
description: Scopri la proprietà SaveFormat di DocSaveOptions per scegliere facilmente tra i formati Doc o Dot per un salvataggio dei documenti senza interruzioni. Ottimizza il tuo flusso di lavoro oggi stesso!
type: docs
weight: 50
url: /it/net/aspose.words.saving/docsaveoptions/saveformat/
---
## DocSaveOptions.SaveFormat property

Specifica il formato in cui il documento verrà salvato se viene utilizzato questo oggetto di opzioni di salvataggio. Può essereDoc ODot .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [DocSaveOptions](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
