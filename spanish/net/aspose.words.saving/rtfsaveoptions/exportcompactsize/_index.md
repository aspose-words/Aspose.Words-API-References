---
title: RtfSaveOptions.ExportCompactSize
linktitle: ExportCompactSize
articleTitle: ExportCompactSize
second_title: Aspose.Words para .NET
description: RtfSaveOptions ExportCompactSize propiedad. Permite reducir el tamaño de los documentos RTF de salida pero si contienen texto RTL de derecha a izquierda no se mostrarán correctamente. El valor predeterminado esFALSO  en C#.
type: docs
weight: 20
url: /es/net/aspose.words.saving/rtfsaveoptions/exportcompactsize/
---
## RtfSaveOptions.ExportCompactSize property

Permite reducir el tamaño de los documentos RTF de salida, pero si contienen texto RTL (de derecha a izquierda), no se mostrarán correctamente. El valor predeterminado es`FALSO` .

```csharp
public bool ExportCompactSize { get; set; }
```

## Observaciones

Si el documento que desea convertir a RTF usando Aspose.Words no contiene texto de derecha a izquierda en idiomas como el árabe, puede configurar esta opción en`verdadero` para reducir el tamaño del RTF resultante.

## Ejemplos

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
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
