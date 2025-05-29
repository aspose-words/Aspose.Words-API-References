---
title: ResourceSavingArgs.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words para .NET
description: Descubra la propiedad de documento ResourceSavingArgs para acceder al objeto de documento actual que se está guardando, mejorando así la eficiencia de su flujo de trabajo.
type: docs
weight: 10
url: /es/net/aspose.words.saving/resourcesavingargs/document/
---
## ResourceSavingArgs.Document property

Obtiene el objeto de documento que se está guardando actualmente.

```csharp
public Document Document { get; }
```

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

* class [Document](../../../aspose.words/document/)
* class [ResourceSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
