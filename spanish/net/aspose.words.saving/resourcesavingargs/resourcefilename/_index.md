---
title: ResourceSavingArgs.ResourceFileName
linktitle: ResourceFileName
articleTitle: ResourceFileName
second_title: Aspose.Words para .NET
description: Gestione sus recursos eficientemente con ResourceSavingArgs. Configure o recupere fácilmente el nombre del archivo para guardar recursos sin la molestia de las rutas.
type: docs
weight: 30
url: /es/net/aspose.words.saving/resourcesavingargs/resourcefilename/
---
## ResourceSavingArgs.ResourceFileName property

Obtiene o establece el nombre del archivo (sin ruta) donde se guardará el recurso.

```csharp
public string ResourceFileName { get; set; }
```

## Observaciones

Esta propiedad le permite redefinir cómo se generan los nombres de los archivos de recursos durante la exportación a HTML o SVG de página fija.

Cuando se activa el evento, esta propiedad contiene el nombre del archivo generado por Aspose.Words. Puede cambiar el valor de esta propiedad para guardar el recurso en un archivo diferente. Tenga en cuenta que los nombres de archivo deben ser únicos.

Aspose.Words genera automáticamente un nombre de archivo único para cada recurso al exportar a formato HTML o SVG de página fija. La forma en que se genera el nombre del archivo de recurso depende de si se guarda el documento en un archivo o en una secuencia.

Al guardar un documento en un archivo, el nombre del archivo de recursos generado se ve así: &lt;nombre del archivo base del documento&gt;.&lt;número de imagen&gt;.&lt;extensión&gt;.

Al guardar un documento en un flujo, el nombre del archivo de recursos generado se ve así: Aspose.Words.&lt;guid del documento&gt;.&lt;número de imagen&gt;.&lt;extensión&gt;.

`ResourceFileName` debe contener solo el nombre del archivo sin la ruta. Aspose.Words determina la ruta para guardar y el valor del`origen` atributo para escribir en HTML o SVG de página fija usando el nombre del archivo del documento, el[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/) o[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/) y[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/) o[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/) propiedades.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

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

* class [ResourceSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
