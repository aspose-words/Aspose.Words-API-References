---
title: MarkdownSaveOptions.ImagesFolder
second_title: Referencia de API de Aspose.Words para .NET
description: MarkdownSaveOptions propiedad. Especifica la carpeta física donde se guardan las imágenes al exportar un documento a elMarkdown formato. El valor predeterminado es una cadena vacía.
type: docs
weight: 40
url: /es/net/aspose.words.saving/markdownsaveoptions/imagesfolder/
---
## MarkdownSaveOptions.ImagesFolder property

Especifica la carpeta física donde se guardan las imágenes al exportar un documento a elMarkdown formato. El valor predeterminado es una cadena vacía.

```csharp
public string ImagesFolder { get; set; }
```

### Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) enMarkdown format, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes. `ImagesFolder` le permite especificar dónde se guardarán las imágenes.

Si guarda un documento en un archivo y proporciona un nombre de archivo, Aspose.Words, de forma predeterminada, guarda las imágenes en la misma carpeta donde se guarda el archivo del documento. Usar`ImagesFolder` para anular este comportamiento.

Si guarda un documento en una secuencia, Aspose.Words no tiene una carpeta donde guardar las imágenes, pero aún necesita guardar las imágenes en algún lugar. En este caso, debe especificar una carpeta accesible en el`ImagesFolder` propiedad.

Si la carpeta especificada por`ImagesFolder` no existe, se creará automáticamente.

### Ver también

* class [MarkdownSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../markdownsaveoptions/)
* asamblea [Aspose.Words](../../../)


