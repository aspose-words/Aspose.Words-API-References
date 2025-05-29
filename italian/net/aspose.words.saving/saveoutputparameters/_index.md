---
title: SaveOutputParameters Class
linktitle: SaveOutputParameters
articleTitle: SaveOutputParameters
second_title: Aspose.Words per .NET
description: Scopri la classe Aspose.Words.Saving.SaveOutputParameters, che fornisce dettagli essenziali dopo il salvataggio del documento, migliorando l'esperienza di gestione dei documenti.
type: docs
weight: 6390
url: /it/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Questo oggetto viene restituito al chiamante dopo il salvataggio di un documento e contiene informazioni aggiuntive che sono state generate o calcolate durante l'operazione di salvataggio. Il chiamante può utilizzare o ignorare questo oggetto.

Per saperne di più, visita il[Salva un documento](https://docs.aspose.com/words/net/save-a-document/) articolo di documentazione.

```csharp
public class SaveOutputParameters
```

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Restituisce la stringa Content-Type (Internet Media Type) che identifica il tipo di documento salvato. |

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

* spazio dei nomi [Aspose.Words.Saving](../../aspose.words.saving/)
* assemblea [Aspose.Words](../../)
