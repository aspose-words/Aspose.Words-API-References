---
title: BuiltInDocumentProperties.Thumbnail
second_title: Aspose.Words per .NET API Reference
description: BuiltInDocumentProperties proprietà. Ottiene o imposta la miniatura del documento.
type: docs
weight: 280
url: /it/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Ottiene o imposta la miniatura del documento.

```csharp
public byte[] Thumbnail { get; set; }
```

### Osservazioni

Per ora questa proprietà viene utilizzata solo quando un documento viene esportato in ePub, non viene letto e scritto in altri formati di documento.

L'immagine di un formato arbitrario può essere impostata su questa proprietà, ma il formato viene verificato durante l'esportazione. InvalidOperationException viene generato se l'immagine non è valida o il suo formato non è supportato per un formato specifico del documento .

Per la pubblicazione ePub possono essere utilizzate solo immagini gif, jpeg e png.

### Esempi

Mostra come aggiungere una miniatura a un documento che salviamo come Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Se salviamo un documento, la cui proprietà "Thumbnail" contiene dati di immagine che abbiamo aggiunto, come Epub,
// un lettore che apre quel documento può visualizzare l'immagine prima della prima pagina.
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
* spazio dei nomi [Aspose.Words.Properties](../../builtindocumentproperties/)
* assemblea [Aspose.Words](../../../)


