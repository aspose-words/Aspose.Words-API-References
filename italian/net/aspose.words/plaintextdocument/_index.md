---
title: Class PlainTextDocument
second_title: Aspose.Words per .NET API Reference
description: Aspose.Words.PlainTextDocument classe. Permette di estrarre la rappresentazione in testo semplice del contenuto del documento.
type: docs
weight: 4440
url: /it/net/aspose.words/plaintextdocument/
---
## PlainTextDocument class

Permette di estrarre la rappresentazione in testo semplice del contenuto del documento.

Per saperne di più, visita il[Lavorare con documenti di testo](https://docs.aspose.com/words/net/working-with-text-document/) articolo di documentazione.

```csharp
public class PlainTextDocument
```

## Costruttori

| Nome | Descrizione |
| --- | --- |
| [PlainTextDocument](plaintextdocument/#constructor)(Stream) | Crea un documento di testo semplice da un flusso. Rileva automaticamente il formato del file. |
| [PlainTextDocument](plaintextdocument/#constructor_2)(string) | Crea un documento di testo semplice da un file. Rileva automaticamente il formato del file. |
| [PlainTextDocument](plaintextdocument/#constructor_1)(Stream, LoadOptions) | Crea un documento di testo semplice da un flusso. Consente di specificare opzioni aggiuntive come una password di crittografia. |
| [PlainTextDocument](plaintextdocument/#constructor_3)(string, LoadOptions) | Crea un documento di testo semplice da un file. Consente di specificare opzioni aggiuntive come una password di crittografia. |

## Proprietà

| Nome | Descrizione |
| --- | --- |
| [BuiltInDocumentProperties](../../aspose.words/plaintextdocument/builtindocumentproperties/) { get; } | Ottiene[`BuiltInDocumentProperties`](./builtindocumentproperties/) del documento. |
| [CustomDocumentProperties](../../aspose.words/plaintextdocument/customdocumentproperties/) { get; } | Ottiene[`CustomDocumentProperties`](./customdocumentproperties/) del documento. |
| [Text](../../aspose.words/plaintextdocument/text/) { get; } | Ottiene il contenuto testuale del documento concatenato come una stringa. |

### Esempi

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

* spazio dei nomi [Aspose.Words](../../aspose.words/)
* assemblea [Aspose.Words](../../)


