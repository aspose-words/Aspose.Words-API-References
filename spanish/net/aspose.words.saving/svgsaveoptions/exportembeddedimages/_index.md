---
title: SvgSaveOptions.ExportEmbeddedImages
linktitle: ExportEmbeddedImages
articleTitle: ExportEmbeddedImages
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad SvgSaveOptions ExportEmbeddedImages le permite incrustar imágenes en archivos SVG como base64, mejorando la portabilidad y al mismo tiempo administrando el tamaño del archivo.
type: docs
weight: 20
url: /es/net/aspose.words.saving/svgsaveoptions/exportembeddedimages/
---
## SvgSaveOptions.ExportEmbeddedImages property

Especifica si las imágenes deben incrustarse en el documento SVG como base64. Tenga en cuenta que activar esta opción puede provocar un aumento significativo en el tamaño del archivo SVG de salida.

```csharp
public bool ExportEmbeddedImages { get; set; }
```

## Ejemplos

Muestra cómo manipular e imprimir las URI de los recursos vinculados creados al convertir un documento a .svg.

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
/// Cuenta e imprime las URI de los recursos contenidos en él a medida que se convierten a .svg.
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

* class [SvgSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
