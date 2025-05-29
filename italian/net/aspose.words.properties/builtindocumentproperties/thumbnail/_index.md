---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: Aspose.Words per .NET
description: Gestisci l'aspetto visivo dei tuoi documenti con BuiltInDocumentProperties. Ottieni o imposta facilmente miniature per una presentazione e un'organizzazione ottimizzate.
type: docs
weight: 310
url: /it/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Ottiene o imposta la miniatura del documento.

```csharp
public byte[] Thumbnail { get; set; }
```

### Eccezioni

| eccezione | condizione |
| --- | --- |
| InvalidOperationException | Generato se l'immagine non è valida o il suo formato non è supportato per il formato specifico del documento. |

## Osservazioni

Per ora questa proprietà viene utilizzata solo quando un documento viene esportato in formato ePub, non viene letta e scritta in altri formati di documento.

È possibile impostare questa proprietà su un'immagine di formato arbitrario, ma il formato viene verificato durante l'esportazione.

Per la pubblicazione ePub è possibile utilizzare solo immagini gif, jpeg e png.

## Esempi

Mostra come aggiungere una miniatura a un documento che salviamo come Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Se salviamo un documento, la cui proprietà "Miniatura" contiene dati di immagine che abbiamo aggiunto, come Epub,
// Un lettore che apre quel documento potrebbe visualizzare l'immagine prima della prima pagina.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// Possiamo estrarre l'immagine in miniatura di un documento e salvarla nel file system locale.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### Guarda anche

* class [BuiltInDocumentProperties](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
