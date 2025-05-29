---
title: ResourceSavingArgs Class
linktitle: ResourceSavingArgs
articleTitle: ResourceSavingArgs
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Saving.ResourceSavingArgs, que mejora el procesamiento de sus documentos al proporcionar datos esenciales para el evento ResourceSaving.
type: docs
weight: 6360
url: /es/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

Proporciona datos para el[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) evento.

Para obtener más información, visite el[Guardar un documento](https://docs.aspose.com/words/net/save-a-document/) Artículo de documentación.

```csharp
public class ResourceSavingArgs
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Obtiene el objeto de documento que se está guardando actualmente. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Especifica si Aspose.Words debe mantener la secuencia abierta o cerrarla después de guardar un recurso. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Obtiene o establece el nombre del archivo (sin ruta) donde se guardará el recurso. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Obtiene o establece el identificador uniforme de recursos (URI) utilizado para hacer referencia al archivo de recursos desde el documento. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Permite especificar la secuencia donde se guardará el recurso. |

## Observaciones

De forma predeterminada, cuando Aspose.Words guarda un documento en formato HTML o SVG de página fija, guarda cada recurso en un archivo independiente. Aspose.Words utiliza el nombre del archivo del documento y un número único para generar un nombre de archivo único para cada recurso del documento.

`ResourceSavingArgs` permite redefinir cómo se generan los nombres de los archivos de recursos o evitar por completo el guardado de recursos en archivos proporcionando sus propios objetos de flujo.

Para aplicar su propia lógica para generar nombres de archivos de recursos, utilice [`ResourceFileName`](./resourcefilename/) propiedad.

Para guardar recursos en secuencias en lugar de archivos, utilice el[`ResourceStream`](./resourcestream/) propiedad.

## Ejemplos

Muestra cómo utilizar una devolución de llamada para rastrear recursos externos creados al convertir un documento a HTML.

```csharp
public void ResourceSavingCallback()
{
    Document doc = new Document(MyDir + "Bullet points with alternative font.docx");

    FontSavingCallback callback = new FontSavingCallback();

    HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions
    {
        ResourceSavingCallback = callback
    };

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

    Console.WriteLine(callback.GetText());
}

private class FontSavingCallback : IResourceSavingCallback
{
    /// <summary>
    /// Se llama cuando Aspose.Words guarda un recurso externo en una página fija HTML o SVG.
    /// </summary>
    public void ResourceSaving(ResourceSavingArgs args)
    {
        mText.AppendLine($"Original document URI:\t{args.Document.OriginalFileName}");
        mText.AppendLine($"Resource being saved:\t{args.ResourceFileName}");
        mText.AppendLine($"Full uri after saving:\t{args.ResourceFileUri}\n");
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private readonly StringBuilder mText = new StringBuilder();
}
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
