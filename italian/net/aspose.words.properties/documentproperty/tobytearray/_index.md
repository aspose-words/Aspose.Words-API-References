---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words per .NET
description: Converti DocumentProperty in un array di byte senza sforzo con il metodo ToByteArray. Semplifica la gestione dei dati e migliora l'efficienza della tua programmazione!
type: docs
weight: 70
url: /it/net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

Restituisce il valore della proprietà come array di byte.

```csharp
public byte[] ToByteArray()
```

## Osservazioni

Genera un'eccezione se il tipo di proprietà non èByteArray.

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

* class [DocumentProperty](../)
* spazio dei nomi [Aspose.Words.Properties](../../../aspose.words.properties/)
* assemblea [Aspose.Words](../../../)
