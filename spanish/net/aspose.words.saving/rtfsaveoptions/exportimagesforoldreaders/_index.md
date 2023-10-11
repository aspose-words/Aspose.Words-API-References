---
title: RtfSaveOptions.ExportImagesForOldReaders
second_title: Referencia de API de Aspose.Words para .NET
description: RtfSaveOptions propiedad. Especifica si las palabras clave para lectores antiguos se escriben en RTF o no. Esto puede afectar significativamente el tamaño del documento RTF. El valor predeterminado esverdadero .
type: docs
weight: 30
url: /es/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

Especifica si las palabras clave para "lectores antiguos" se escriben en RTF o no. Esto puede afectar significativamente el tamaño del documento RTF. El valor predeterminado es`verdadero` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

### Observaciones

Los "lectores antiguos" son aplicaciones anteriores a Microsoft Word 97 y también WordPad. Cuando esta opción está activada`verdadero` Aspose.Words escribe palabras clave RTF adicionales. Estas palabras clave permiten que el documento se muestre correctamente cuando se abre en una aplicación "lector antiguo", pero pueden aumentar significativamente el tamaño del documento.

Si configura esta opción en`FALSO`, entonces sólo se mostrarán imágenes en formatos WMF, EMF y BMP en los "lectores antiguos".

### Ejemplos

Muestra cómo guardar un documento en .rtf con opciones personalizadas.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crea un objeto "RtfSaveOptions" para pasarlo al método "Guardar" del documento para modificar cómo lo guardamos en un RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Establece la propiedad "ExportCompactSize" en "true" para
// reduce el tamaño del documento guardado a costa de la compatibilidad del texto de derecha a izquierda.
options.ExportCompactSize = true;

// Establece la propiedad "ExportImagesFotOldReaders" en "true" para usar palabras clave adicionales para garantizar que nuestro documento sea
// compatible con lectores anteriores a Microsoft Word 97 y WordPad.
// Establece la propiedad "ExportImagesFotOldReaders" en "false" para reducir el tamaño del documento,
// pero evita que los lectores antiguos puedan leer cualquier imagen BMP o que no sea un metarchivo que pueda contener el documento.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Ver también

* class [RtfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../rtfsaveoptions/)
* asamblea [Aspose.Words](../../../)


