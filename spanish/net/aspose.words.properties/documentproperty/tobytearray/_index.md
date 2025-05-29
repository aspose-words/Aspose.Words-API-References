---
title: DocumentProperty.ToByteArray
linktitle: ToByteArray
articleTitle: ToByteArray
second_title: Aspose.Words para .NET
description: Convierte DocumentProperty en una matriz de bytes fácilmente con el método ToByteArray. ¡Optimiza la gestión de datos y mejora la eficiencia de tu codificación!
type: docs
weight: 70
url: /es/net/aspose.words.properties/documentproperty/tobytearray/
---
## DocumentProperty.ToByteArray method

Devuelve el valor de la propiedad como una matriz de bytes.

```csharp
public byte[] ToByteArray()
```

## Observaciones

Lanza una excepción si el tipo de propiedad no esByteArray.

## Ejemplos

Muestra cómo agregar una miniatura a un documento que guardamos como Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Si guardamos un documento, cuya propiedad "Miniatura" contiene datos de imágenes que agregamos, como un Epub,
// un lector que abre ese documento puede mostrar la imagen antes de la primera página.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

//Podemos extraer la imagen en miniatura de un documento y guardarla en el sistema de archivos local.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### Ver también

* class [DocumentProperty](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
