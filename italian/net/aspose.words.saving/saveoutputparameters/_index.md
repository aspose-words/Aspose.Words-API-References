---
title: Class SaveOutputParameters
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.Saving.SaveOutputParameters classe. Questo oggetto viene restituito al chiamante dopo il salvataggio di un documento e contiene informazioni aggiuntive che è stato generato o calcolato durante loperazione di salvataggio. Il chiamante può utilizzare o ignorare questo oggetto.
type: docs
weight: 5310
url: /it/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Questo oggetto viene restituito al chiamante dopo il salvataggio di un documento e contiene informazioni aggiuntive che è stato generato o calcolato durante l'operazione di salvataggio. Il chiamante può utilizzare o ignorare questo oggetto.

```csharp
public class SaveOutputParameters
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Restituisce la stringa Content-Type (Internet Media Type) che identifica il tipo del documento salvato. |

### Esempi

Mostra come accedere ai parametri di output dell'operazione di salvataggio di un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Dopo aver salvato un documento, possiamo accedere al tipo di supporto Internet (tipo MIME) del documento di output appena creato.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Questa proprietà cambia a seconda del formato di salvataggio.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Guarda anche

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)


