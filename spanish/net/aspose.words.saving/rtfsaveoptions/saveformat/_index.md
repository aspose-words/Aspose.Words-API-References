---
title: RtfSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: Aspose.Words para .NET
description: Descubra la propiedad SaveFormat de RtfSaveOptions para guardar sin esfuerzo sus documentos en formato RTF, garantizando la compatibilidad y una fácil compartición.
type: docs
weight: 40
url: /es/net/aspose.words.saving/rtfsaveoptions/saveformat/
---
## RtfSaveOptions.SaveFormat property

Especifica el formato en el que se guardará el documento si se utiliza este objeto de opciones de guardado. Solo se puedeRtf .

```csharp
public override SaveFormat SaveFormat { get; set; }
```

## Ejemplos

Muestra cómo guardar un documento en .rtf con opciones personalizadas.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crea un objeto "RtfSaveOptions" para pasar al método "Guardar" del documento para modificar cómo lo guardamos en RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Establezca la propiedad "ExportCompactSize" en "verdadero" para
// reducir el tamaño del documento guardado a costa de la compatibilidad del texto de derecha a izquierda.
options.ExportCompactSize = true;

// Establezca la propiedad "ExportImagesFotOldReaders" en "true" para usar palabras clave adicionales para garantizar que nuestro documento sea
// compatible con lectores anteriores a Microsoft Word 97 y WordPad.
// Establezca la propiedad "ExportImagesFotOldReaders" en "false" para reducir el tamaño del documento,
// pero evita que los lectores antiguos puedan leer cualquier imagen que no sea un metarchivo o BMP que el documento pueda contener.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Ver también

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [RtfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
