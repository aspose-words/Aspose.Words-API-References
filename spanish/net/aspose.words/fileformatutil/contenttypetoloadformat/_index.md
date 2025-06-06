---
title: FileFormatUtil.ContentTypeToLoadFormat
linktitle: ContentTypeToLoadFormat
articleTitle: ContentTypeToLoadFormat
second_title: Aspose.Words para .NET
description: Transforme fácilmente los tipos de contenido IANA en valores de formato de carga con el método FileFormatUtil ContentTypeToLoadFormat. ¡Simplifique la gestión de sus archivos hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words/fileformatutil/contenttypetoloadformat/
---
## FileFormatUtil.ContentTypeToLoadFormat method

Convierte el tipo de contenido de IANA en un valor enumerado con formato de carga.

```csharp
public static LoadFormat ContentTypeToLoadFormat(string contentType)
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentException | Se lanza cuando no se puede convertir. |

## Ejemplos

Muestra cómo encontrar el formato de carga/guardado de Aspose correspondiente a cada cadena de tipo de medio.

```csharp
 // Los métodos ContentTypeToSaveFormat/ContentTypeToLoadFormat solo aceptan nombres de tipos de medios oficiales de IANA, también conocidos como tipos MIME.
// Todos los tipos de medios válidos se enumeran aquí: https://www.iana.org/assignments/media-types/media-types.xhtml.

Intentar asociar un SaveFormat con una cadena de tipo de medio parcial no funcionará.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("jpeg"));

// Si Aspose.Words no tiene un formato de guardado/carga correspondiente para un tipo de contenido, también se lanzará una excepción.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToSaveFormat("application/zip"));

// Los archivos de los tipos enumerados a continuación se pueden guardar, pero no cargar mediante Aspose.Words.
Assert.Throws<ArgumentException>(() => FileFormatUtil.ContentTypeToLoadFormat("image/jpeg"));

Assert.AreEqual(SaveFormat.Jpeg, FileFormatUtil.ContentTypeToSaveFormat("image/jpeg"));
Assert.AreEqual(SaveFormat.Png, FileFormatUtil.ContentTypeToSaveFormat("image/png"));
Assert.AreEqual(SaveFormat.Tiff, FileFormatUtil.ContentTypeToSaveFormat("image/tiff"));
Assert.AreEqual(SaveFormat.Gif, FileFormatUtil.ContentTypeToSaveFormat("image/gif"));
Assert.AreEqual(SaveFormat.Emf, FileFormatUtil.ContentTypeToSaveFormat("image/x-emf"));
Assert.AreEqual(SaveFormat.Xps, FileFormatUtil.ContentTypeToSaveFormat("application/vnd.ms-xpsdocument"));
Assert.AreEqual(SaveFormat.Pdf, FileFormatUtil.ContentTypeToSaveFormat("application/pdf"));
Assert.AreEqual(SaveFormat.Svg, FileFormatUtil.ContentTypeToSaveFormat("image/svg+xml"));
Assert.AreEqual(SaveFormat.Epub, FileFormatUtil.ContentTypeToSaveFormat("application/epub+zip"));

// Para los tipos de archivos que se pueden guardar y cargar, podemos hacer coincidir un tipo de medio con un formato de carga y un formato de guardado.
Assert.AreEqual(LoadFormat.Doc, FileFormatUtil.ContentTypeToLoadFormat("application/msword"));
Assert.AreEqual(SaveFormat.Doc, FileFormatUtil.ContentTypeToSaveFormat("application/msword"));

Assert.AreEqual(LoadFormat.Docx,
    FileFormatUtil.ContentTypeToLoadFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));
Assert.AreEqual(SaveFormat.Docx,
    FileFormatUtil.ContentTypeToSaveFormat(
        "application/vnd.openxmlformats-officedocument.wordprocessingml.document"));

Assert.AreEqual(LoadFormat.Text, FileFormatUtil.ContentTypeToLoadFormat("text/plain"));
Assert.AreEqual(SaveFormat.Text, FileFormatUtil.ContentTypeToSaveFormat("text/plain"));

Assert.AreEqual(LoadFormat.Rtf, FileFormatUtil.ContentTypeToLoadFormat("application/rtf"));
Assert.AreEqual(SaveFormat.Rtf, FileFormatUtil.ContentTypeToSaveFormat("application/rtf"));

Assert.AreEqual(LoadFormat.Html, FileFormatUtil.ContentTypeToLoadFormat("text/html"));
Assert.AreEqual(SaveFormat.Html, FileFormatUtil.ContentTypeToSaveFormat("text/html"));

Assert.AreEqual(LoadFormat.Mhtml, FileFormatUtil.ContentTypeToLoadFormat("multipart/related"));
Assert.AreEqual(SaveFormat.Mhtml, FileFormatUtil.ContentTypeToSaveFormat("multipart/related"));
```

### Ver también

* enum [LoadFormat](../../loadformat/)
* class [FileFormatUtil](../)
* espacio de nombres [Aspose.Words](../../../aspose.words/)
* asamblea [Aspose.Words](../../../)
