---
title: RtfSaveOptions.ExportCompactSize
linktitle: ExportCompactSize
articleTitle: ExportCompactSize
second_title: Aspose.Words para .NET
description: Optimice el tamaño de los documentos RTF con la propiedad ExportCompactSize. Garantice un almacenamiento eficiente manteniendo la integridad del texto, incluso con contenido RTL.
type: docs
weight: 20
url: /es/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Permite hacer que los documentos RTF de salida sean más pequeños, pero si contienen texto RTL (de derecha a izquierda), no se mostrará correctamente. El valor predeterminado es`FALSO` .

```csharp
public bool ExportCompactSize { get; set; }
```

## Observaciones

Si el documento que desea convertir a RTF mediante Aspose.Words no contiene texto de derecha a izquierda en idiomas como el árabe, puede configurar esta opción en`verdadero` para reducir el tamaño del RTF resultante.

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
