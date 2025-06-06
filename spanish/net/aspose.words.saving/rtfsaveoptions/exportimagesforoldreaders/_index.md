---
title: RtfSaveOptions.ExportImagesForOldReaders
linktitle: ExportImagesForOldReaders
articleTitle: ExportImagesForOldReaders
second_title: Aspose.Words para .NET
description: Optimice sus documentos RTF con la propiedad ExportImagesForOldReaders. Controle la inclusión de palabras clave para lectores antiguos, lo que afecta el tamaño y el rendimiento del archivo.
type: docs
weight: 30
url: /es/net/aspose.words.saving/rtfsaveoptions/exportimagesforoldreaders/
---
## RtfSaveOptions.ExportImagesForOldReaders property

Especifica si las palabras clave para "lectores antiguos" se escriben en RTF o no. Esto puede afectar significativamente el tamaño del documento RTF. El valor predeterminado es`verdadero` .

```csharp
public bool ExportImagesForOldReaders { get; set; }
```

## Observaciones

Los "lectores antiguos" son aplicaciones anteriores a Microsoft Word 97 y también WordPad. Cuando esta opción está`verdadero` Aspose.Words escribe palabras clave RTF adicionales. Estas palabras clave permiten que el documento se muestre correctamente cuando se abre en una aplicación de "lectura antigua", pero pueden aumentar significativamente el tamaño del documento.

Si configura esta opción en`FALSO`entonces sólo se mostrarán las imágenes en formatos WMF, EMF y BMP en "lectores antiguos".

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

* class [RtfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
