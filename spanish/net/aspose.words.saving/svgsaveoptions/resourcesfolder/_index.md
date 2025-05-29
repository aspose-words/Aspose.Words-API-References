---
title: SvgSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words para .NET
description: Descubra cómo configurar la carpeta Recursos en SvgSaveOptions para un almacenamiento de imágenes eficiente al exportar documentos a formato SVG. ¡Optimice su flujo de trabajo hoy mismo!
type: docs
weight: 80
url: /es/net/aspose.words.saving/svgsaveoptions/resourcesfolder/
---
## SvgSaveOptions.ResourcesFolder property

Especifica la carpeta física donde se guardan los recursos (imágenes) al exportar un documento al formato Svg. El valor predeterminado es`nulo` .

```csharp
public string ResourcesFolder { get; set; }
```

## Observaciones

Tiene efecto sólo si[`ExportEmbeddedImages`](../exportembeddedimages/) La propiedad es`FALSO`.

Cuando guardas un[`Document`](../../../aspose.words/document/) en formato SVG, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes.`ResourcesFolder` le permite especificar dónde se guardarán las imágenes y[`ResourcesFolderAlias`](../resourcesfolderalias/) permite especificar cómo se construirán las URI de las imágenes.

Si guarda un documento en un archivo y proporciona un nombre de archivo, Aspose.Words, de forma predeterminada, guarda las imágenes en la misma carpeta donde se guarda el archivo del documento. Utilice`ResourcesFolder` para anular este comportamiento.

Si guarda un documento en una secuencia, Aspose.Words no tiene una carpeta donde guardar las imágenes, pero aun así necesita guardarlas en algún lugar. En este caso, debe especificar una carpeta accesible en el archivo.`ResourcesFolder` propiedad

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
