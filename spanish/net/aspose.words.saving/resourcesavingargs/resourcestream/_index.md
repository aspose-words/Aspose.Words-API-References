---
title: ResourceSavingArgs.ResourceStream
linktitle: ResourceStream
articleTitle: ResourceStream
second_title: Aspose.Words para .NET
description: Descubra la propiedad ResourceStream de ResourceSavingArgs para definir fácilmente dónde se guardan sus recursos, mejorando la eficiencia y el control en sus proyectos.
type: docs
weight: 50
url: /es/net/aspose.words.saving/resourcesavingargs/resourcestream/
---
## ResourceSavingArgs.ResourceStream property

Permite especificar la secuencia donde se guardará el recurso.

```csharp
public Stream ResourceStream { get; set; }
```

## Observaciones

Esta propiedad le permite guardar recursos en transmisiones en lugar de archivos.

El valor predeterminado es`nulo` . Cuando esta propiedad es`nulo` , el recurso se guardará en un archivo especificado en el[`ResourceFileName`](../resourcefilename/) propiedad.

Usando[`IResourceSavingCallback`](../../iresourcesavingcallback/) No se puede sustituir un recurso por otro . Su propósito es únicamente controlar la ubicación donde se guardan los recursos.

## Ejemplos

Muestra cómo utilizar una devolución de llamada para imprimir las URI de recursos externos creados al convertir un documento a HTML.

```csharp
public void HtmlFixedResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ResourceUriPrinter callback = new ResourceUriPrinter();

    HtmlFixedSaveOptions options = new HtmlFixedSaveOptions
    {
        SaveFormat = SaveFormat.HtmlFixed,
        ExportEmbeddedImages = false,
        ResourcesFolder = ArtifactsDir + "HtmlFixedResourceFolder",
        ResourcesFolderAlias = ArtifactsDir + "HtmlFixedResourceFolderAlias",
        ShowPageBorder = false,
        ResourceSavingCallback = callback
    };

    // Una carpeta especificada por ResourcesFolderAlias contendrá los recursos en lugar de ResourcesFolder.
    //Debemos asegurarnos de que la carpeta exista antes de que los flujos puedan poner sus recursos en ella.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HtmlFixedResourceFolder.html", options);

    Console.WriteLine(callback.GetText());

    string[] resourceFiles = Directory.GetFiles(ArtifactsDir + "HtmlFixedResourceFolderAlias");

    Assert.False(Directory.Exists(ArtifactsDir + "HtmlFixedResourceFolder"));
    Assert.AreEqual(6, resourceFiles.Count(f => f.EndsWith(".jpeg") || f.EndsWith(".png") || f.EndsWith(".css")));
}

/// <summary>
/// Cuenta e imprime las URI de los recursos contenidos en él a medida que se convierten a HTML fijo.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        // Si establecemos un alias de carpeta en el objeto SaveOptions, podremos imprimirlo desde aquí.
        mText.AppendLine($"Resource #{++mSavedResourceCount} \"{args.ResourceFileName}\"");

        string extension = Path.GetExtension(args.ResourceFileName);
        switch (extension)
        {
            case ".ttf":
            case ".woff":
            {
                // De forma predeterminada, 'ResourceFileUri' utiliza la carpeta del sistema para las fuentes.
                // Para evitar problemas en otras plataformas debes especificar explícitamente la ruta de las fuentes.
                args.ResourceFileUri = ArtifactsDir + Path.DirectorySeparatorChar + args.ResourceFileName;
                break;
            }
        }

        mText.AppendLine("\t" + args.ResourceFileUri);

        // Si hemos especificado una carpeta en la propiedad "ResourcesFolderAlias",
        // También necesitaremos redirigir cada flujo para colocar su recurso en esa carpeta.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public string GetText()
    {
        return mText.ToString();
    }

    private int mSavedResourceCount;
    private readonly StringBuilder mText = new StringBuilder();
}
```

### Ver también

* class [ResourceSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
