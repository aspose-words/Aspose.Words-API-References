---
title: Class ResourceSavingArgs
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.ResourceSavingArgs clase. Proporciona datos para elResourceSaving evento.
type: docs
weight: 5280
url: /es/net/aspose.words.saving/resourcesavingargs/
---
## ResourceSavingArgs class

Proporciona datos para el[`ResourceSaving`](../iresourcesavingcallback/resourcesaving/) evento.

```csharp
public class ResourceSavingArgs
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Document](../../aspose.words.saving/resourcesavingargs/document/) { get; } | Obtiene el objeto de documento que se está guardando actualmente. |
| [KeepResourceStreamOpen](../../aspose.words.saving/resourcesavingargs/keepresourcestreamopen/) { get; set; } | Especifica si Aspose.Words debe mantener la secuencia abierta o cerrarla después de guardar un recurso. |
| [ResourceFileName](../../aspose.words.saving/resourcesavingargs/resourcefilename/) { get; set; } | Obtiene o establece el nombre del archivo (sin la ruta) donde se guardará el recurso. |
| [ResourceFileUri](../../aspose.words.saving/resourcesavingargs/resourcefileuri/) { get; set; } | Obtiene o establece el identificador uniforme de recursos (URI) utilizado para hacer referencia al archivo de recursos del documento. |
| [ResourceStream](../../aspose.words.saving/resourcesavingargs/resourcestream/) { get; set; } | Permite especificar el flujo donde se guardará el recurso. |

### Observaciones

De forma predeterminada, cuando Aspose.Words guarda un documento en una página fija HTML o SVG, guarda cada recurso en en un archivo separado. Aspose.Words usa el nombre de archivo del documento y un número único para generar un nombre de archivo único para cada recurso encontrado en el documento.

`ResourceSavingArgs` permite redefinir cómo se generan los nombres de los archivos de recursos o eludir por completo el almacenamiento de recursos en archivos proporcionando sus propios objetos de flujo.

Para aplicar su propia lógica para generar nombres de archivos de recursos, use [`ResourceFileName`](./resourcefilename/) propiedad.

Para guardar recursos en flujos en lugar de archivos, use el[`ResourceStream`](./resourcestream/) propiedad.

### Ejemplos

Muestra cómo utilizar una devolución de llamada para realizar un seguimiento de los recursos externos creados al convertir un documento a HTML.

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
    /// Llamado cuando Aspose.Words guarda un recurso externo en una página fija HTML o SVG.
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


