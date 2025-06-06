---
title: SaveOutputParameters Class
linktitle: SaveOutputParameters
articleTitle: SaveOutputParameters
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Saving.SaveOutputParameters, que proporciona detalles esenciales después de guardar el documento, mejorando su experiencia de gestión de documentos.
type: docs
weight: 6390
url: /es/net/aspose.words.saving/saveoutputparameters/
---
## SaveOutputParameters class

Este objeto se devuelve al usuario que llama después de guardar un documento y contiene información adicional generada o calculada durante la operación de guardado. El usuario puede usar o ignorar este objeto.

Para obtener más información, visite el[Guardar un documento](https://docs.aspose.com/words/net/save-a-document/) Artículo de documentación.

```csharp
public class SaveOutputParameters
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [ContentType](../../aspose.words.saving/saveoutputparameters/contenttype/) { get; } | Devuelve la cadena de tipo de contenido (tipo de medio de Internet) que identifica el tipo de documento guardado. |

## Ejemplos

Muestra cómo acceder a los parámetros de salida de la operación de guardado de un documento.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Después de guardar un documento, podemos acceder al tipo de medio de Internet (tipo MIME) del documento de salida recién creado.
SaveOutputParameters parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.doc");

Assert.AreEqual("application/msword", parameters.ContentType);

// Esta propiedad cambia dependiendo del formato de guardado.
parameters = doc.Save(ArtifactsDir + "Document.SaveOutputParameters.pdf");

Assert.AreEqual("application/pdf", parameters.ContentType);
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
