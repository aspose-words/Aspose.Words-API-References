---
title: BuiltInDocumentProperties.Thumbnail
linktitle: Thumbnail
articleTitle: Thumbnail
second_title: Aspose.Words para .NET
description: Gestione el atractivo visual de sus documentos con BuiltInDocumentProperties. Obtenga o configure fácilmente miniaturas para una presentación y organización mejoradas.
type: docs
weight: 310
url: /es/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Obtiene o establece la miniatura del documento.

```csharp
public byte[] Thumbnail { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| InvalidOperationException | Se lanza si la imagen no es válida o su formato no es compatible con el formato específico del documento. |

## Observaciones

Por ahora, esta propiedad se utiliza solo cuando se exporta un documento a ePub, no se lee ni se escribe en otros formatos de documento.

Se puede configurar esta propiedad para una imagen de formato arbitrario, pero el formato se verifica durante la exportación.

Sólo se pueden utilizar imágenes gif, jpeg y png para la publicación ePub.

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

* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../../aspose.words.properties/)
* asamblea [Aspose.Words](../../../)
