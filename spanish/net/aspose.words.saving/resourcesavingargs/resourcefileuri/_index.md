---
title: ResourceSavingArgs.ResourceFileUri
second_title: Referencia de API de Aspose.Words para .NET
description: ResourceSavingArgs propiedad. Obtiene o establece el identificador uniforme de recursos URI utilizado para hacer referencia al archivo de recursos del documento.
type: docs
weight: 40
url: /es/net/aspose.words.saving/resourcesavingargs/resourcefileuri/
---
## ResourceSavingArgs.ResourceFileUri property

Obtiene o establece el identificador uniforme de recursos (URI) utilizado para hacer referencia al archivo de recursos del documento.

```csharp
public string ResourceFileUri { get; set; }
```

### Observaciones

Esta propiedad le permite cambiar los URI de los archivos de recursos exportados a documentos HTML o SVG de página fija.

Aspose.Words genera automáticamente un URI para cada archivo de recursos durante la exportación a formato HTML de página fija o SVG. Los URI generados hacen referencia a archivos de recursos guardados por Aspose.Words. Sin embargo, los URI pueden ser incorrectos si los archivos de recursos se van a mover a otra ubicación o si los archivos de recursos se guardan en secuencias. Esta propiedad permite corregir los URI en estos casos.

Cuando se activa el evento, esta propiedad contiene el URI generado por Aspose.Words. Puede cambiar el valor de esta propiedad para proporcionar un URI personalizado para el archivo de recursos.

[`ResourcesFolder`](../../htmlfixedsaveoptions/resourcesfolder/)[`ResourcesFolder`](../../svgsaveoptions/resourcesfolder/)[`ResourcesFolderAlias`](../../htmlfixedsaveoptions/resourcesfolderalias/)[`ResourcesFolderAlias`](../../svgsaveoptions/resourcesfolderalias/)

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
* espacio de nombres [Aspose.Words.Saving](../../resourcesavingargs/)
* asamblea [Aspose.Words](../../../)


