---
title: SaveOutputParameters.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: Aspose.Words per .NET
description: Scopri la proprietà ContentType di SaveOutputParameters, che fornisce il tipo di supporto Internet per i documenti salvati, garantendo un'identificazione precisa dei file.
type: docs
weight: 10
url: /it/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

Restituisce la stringa Content-Type (Internet Media Type) che identifica il tipo di documento salvato.

```csharp
public string ContentType { get; }
```

## Esempi

Mostra come accedere ai parametri di output dell'operazione di salvataggio di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Dopo aver salvato un documento, possiamo accedere al tipo MIME (Internet Media Type) del documento di output appena creato.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Questa proprietà cambia a seconda del formato di salvataggio.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Guarda anche

* class [SaveOutputParameters](../)
* spazio dei nomi [Aspose.Words.Saving](../../../aspose.words.saving/)
* assemblea [Aspose.Words](../../../)
