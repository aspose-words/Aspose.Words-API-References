---
title: RtfSaveOptions.ExportCompactSize
second_title: Referencia de API de Aspose.Words para .NET
description: RtfSaveOptions propiedad. Permite reducir el tamaño de los documentos RTF de salida pero si contienen texto RTL de derecha a izquierda no se mostrará correctamente. El valor predeterminado esfalso .
type: docs
weight: 20
url: /es/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Permite reducir el tamaño de los documentos RTF de salida, pero si contienen texto RTL (de derecha a izquierda), no se mostrará correctamente. El valor predeterminado es`falso` .

```csharp
public bool ExportCompactSize { get; set; }
```

### Observaciones

Si el documento que desea convertir a RTF usando Aspose.Words no contiene texto de derecha a izquierda en idiomas como el árabe, entonces puede establecer esta opción en`verdadero` para reducir el tamaño del RTF resultante.

### Ejemplos

Muestra cómo guardar un documento en .rtf con opciones personalizadas.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Crear un objeto "RtfSaveOptions" para pasar al método "Guardar" del documento para modificar cómo lo guardamos en un RTF.
RtfSaveOptions options = new RtfSaveOptions();

Assert.AreEqual(SaveFormat.Rtf, options.SaveFormat);

// Establecer la propiedad "Exportar tamaño compacto" en "verdadero" para
// reducir el tamaño del documento guardado a costa de la compatibilidad de texto de derecha a izquierda.
options.ExportCompactSize = true;

// Establezca la propiedad "ExportImagesFotOldReaders" en "true" para usar palabras clave adicionales para garantizar que nuestro documento sea
// compatible con lectores anteriores a Microsoft Word 97 y WordPad.
// Establecer la propiedad "ExportImagesFotOldReaders" en "falso" para reducir el tamaño del documento,
// pero evita que los lectores antiguos puedan leer cualquier imagen que no sea un metarchivo o BMP que pueda contener el documento.
options.ExportImagesForOldReaders = exportImagesForOldReaders;

doc.Save(ArtifactsDir + "RtfSaveOptions.ExportImages.rtf", options);
```

### Ver también

* class [RtfSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../rtfsaveoptions/)
* asamblea [Aspose.Words](../../../)


