---
title: DocumentProperty.ToByteArray
second_title: Aspose.Words per .NET API Reference
description: DocumentProperty metodo. Restituisce il valore della proprietà come matrice di byte.
type: docs
weight: 70
url: /it/net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

Restituisce il valore della proprietà come matrice di byte.

```csharp
public byte[] ToByteArray()
```

### Osservazioni

Genera un'eccezione se il tipo di proprietà non lo èByteArray.

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

* class [DocumentProperty](../)
* spazio dei nomi [Aspose.Words.Properties](../../documentproperty/)
* assemblea [Aspose.Words](../../../)


