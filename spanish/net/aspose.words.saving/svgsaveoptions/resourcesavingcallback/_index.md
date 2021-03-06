---
title: ResourceSavingCallback
second_title: Referencia de API de Aspose.Words para .NET
description: Permite controlar cómo se guardan los recursos imágenes cuando un documento se exporta a formato SVG.
type: docs
weight: 40
url: /es/net/aspose.words.saving/svgsaveoptions/resourcesavingcallback/
---
## SvgSaveOptions.ResourceSavingCallback property

Permite controlar cómo se guardan los recursos (imágenes) cuando un documento se exporta a formato SVG.

```csharp
public IResourceSavingCallback ResourceSavingCallback { get; set; }
```

### Ejemplos

Muestra cómo manipular e imprimir los URI de los recursos vinculados creados al convertir un documento a .svg.

```csharp
public void SvgResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    SvgSaveOptions options = new SvgSaveOptions
    {
        SaveFormat = SaveFormat.Svg,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "SvgResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "SvgResourceFolderAlias",
        ShowPageBorder = false,

        ResourceSavingCallback = new ResourceUriPrinter()
    };

    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "SvgSaveOptions.SvgResourceFolder.svg", options);
}

/// <summary>
/// Cuenta e imprime los URI de los recursos contenidos en cuando se convierten a .svg.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Console.WriteLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");
        Console.WriteLine("\t" + args.ResourceFileUri);
    }

    private int mSavedResourceCount;
}
```

### Ver también

* interface [IResourceSavingCallback](../../iresourcesavingcallback)
* class [SvgSaveOptions](../../svgsaveoptions)
* espacio de nombres [Aspose.Words.Saving](../../svgsaveoptions)
* asamblea [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
