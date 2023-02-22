---
title: BuiltInDocumentProperties.Thumbnail
second_title: Referencia de API de Aspose.Words para .NET
description: BuiltInDocumentProperties propiedad. Obtiene o establece la miniatura del documento.
type: docs
weight: 280
url: /es/net/aspose.words.properties/builtindocumentproperties/thumbnail/
---
## BuiltInDocumentProperties.Thumbnail property

Obtiene o establece la miniatura del documento.

```csharp
public byte[] Thumbnail { get; set; }
```

### Observaciones

Por ahora, esta propiedad se usa solo cuando un documento se exporta a ePub, no se lee ni se escribe en otros formatos de documento.

La imagen de formato arbitrario se puede establecer en esta propiedad, pero el formato se comprueba durante la exportación. InvalidOperationException se lanza si la imagen no es válida o su formato no es compatible con formato específico del documento.

Solo se pueden usar imágenes gif, jpeg y png para la publicación ePub.

### Ejemplos

Muestra cómo agregar una miniatura a un documento que guardamos como Epub.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Si guardamos un documento, cuya propiedad "Miniatura" contiene datos de imagen que agregamos, como un Epub,
// un lector que abre ese documento puede mostrar la imagen antes de la primera página.
BuiltInDocumentProperties properties = doc.BuiltInDocumentProperties;

byte[] thumbnailBytes = File.ReadAllBytes(ImageDir + "Logo.jpg");
properties.Thumbnail = thumbnailBytes;

doc.Save(ArtifactsDir + "DocumentProperties.Thumbnail.epub");

// Podemos extraer la imagen en miniatura de un documento y guardarlo en el sistema de archivos local.
DocumentProperty thumbnail = doc.BuiltInDocumentProperties["Thumbnail"];
File.WriteAllBytes(ArtifactsDir + "DocumentProperties.Thumbnail.gif", thumbnail.ToByteArray());
```

### Ver también

* class [BuiltInDocumentProperties](../)
* espacio de nombres [Aspose.Words.Properties](../../builtindocumentproperties/)
* asamblea [Aspose.Words](../../../)


