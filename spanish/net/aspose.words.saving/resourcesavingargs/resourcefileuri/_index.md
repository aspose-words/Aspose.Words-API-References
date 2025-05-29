---
title: ResourceSavingArgs.ResourceFileUri
linktitle: ResourceFileUri
articleTitle: ResourceFileUri
second_title: Aspose.Words para .NET
description: Descubra la propiedad ResourceFileUri de ResourceSavingArgs para administrar y referenciar fácilmente los archivos de recursos en sus documentos. ¡Mejore su eficiencia hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

Obtiene o establece el identificador uniforme de recursos (URI) utilizado para hacer referencia al archivo de recursos desde el documento.

```csharp
public string ResourceFileUri { get; set; }
```

## Observaciones

Esta propiedad le permite cambiar las URI de los archivos de recursos exportados a documentos HTML o SVG de página fija.

Aspose.Words genera automáticamente una URI para cada archivo de recurso durante la exportación a formato HTML o SVG de página fija. Las URI generadas hacen referencia a los archivos de recursos guardados por Aspose.Words. Sin embargo, las URI pueden ser incorrectas si los archivos de recursos se mueven a otra ubicación o se guardan en secuencias. Esta propiedad permite corregir las URI en estos casos.

Cuando se activa el evento, esta propiedad contiene la URI generada por Aspose.Words. Puede cambiar el valor de esta propiedad para proporcionar una URI personalizada para el archivo de recursos.

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
