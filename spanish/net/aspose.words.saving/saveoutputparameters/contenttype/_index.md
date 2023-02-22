---
title: SaveOutputParameters.ContentType
second_title: Referencia de API de Aspose.Words para .NET
description: SaveOutputParameters propiedad. Devuelve la cadena de tipo de contenido Tipo de medio de Internet que identifica el tipo del documento guardado.
type: docs
weight: 10
url: /es/net/aspose.words.saving/saveoutputparameters/contenttype/
---
## SaveOutputParameters.ContentType property

Devuelve la cadena de tipo de contenido (Tipo de medio de Internet) que identifica el tipo del documento guardado.

```csharp
public string ContentType { get; }
```

### Ejemplos

Muestra cómo acceder a los parámetros de salida de la operación de guardado de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Después de guardar un documento, podemos acceder al tipo de medio de Internet (tipo MIME) del documento de salida recién creado.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Esta propiedad cambia según el formato de guardado.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Ver también

* class [SaveOutputParameters](../)
* espacio de nombres [Aspose.Words.Saving](../../saveoutputparameters/)
* asamblea [Aspose.Words](../../../)


