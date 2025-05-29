---
title: PlainTextDocument.Text
linktitle: Text
articleTitle: Text
second_title: Aspose.Words per .NET
description: Accedi alla proprietà text di PlainTextDocument per recuperare il contenuto del documento come un'unica stringa, migliorando la gestione e l'analisi dei dati.
type: docs
weight: 40
url: /it/net/aspose.words/plaintextdocument/text/
---
## PlainTextDocument.Text property

Ottiene il contenuto testuale del documento concatenato come stringa.

```csharp
public string Text { get; }
```

## Esempi

Mostra come caricare il contenuto di un documento Microsoft Word in testo normale.

```csharp
Document doc = new Document(); 
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

doc.Save(ArtifactsDir + "PlainTextDocument.Load.docx");

PlainTextDocument plaintext = new PlainTextDocument(ArtifactsDir + "PlainTextDocument.Load.docx");

Assert.AreEqual("Hello world!", plaintext.Text.Trim());
```

### Guarda anche

* class [PlainTextDocument](../)
* spazio dei nomi [Aspose.Words](../../../aspose.words/)
* assemblea [Aspose.Words](../../../)
