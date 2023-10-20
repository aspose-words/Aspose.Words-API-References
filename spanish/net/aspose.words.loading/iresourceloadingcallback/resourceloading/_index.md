---
title: IResourceLoadingCallback.ResourceLoading
linktitle: ResourceLoading
articleTitle: ResourceLoading
second_title: Aspose.Words para .NET
description: IResourceLoadingCallback ResourceLoading método. Se llama cuando Aspose.Words carga cualquier recurso externo en C#.
type: docs
weight: 10
url: /es/net/aspose.words.loading/iresourceloadingcallback/resourceloading/
---
## IResourceLoadingCallback.ResourceLoading method

Se llama cuando Aspose.Words carga cualquier recurso externo.

```csharp
public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
```

## Ejemplos

Muestra cómo personalizar el proceso de carga de recursos externos en un documento.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Las imágenes normalmente se insertan mediante un URI o una matriz de bytes.
    // Cada instancia de una carga de recursos llamará al método ResourceLoading de nuestra devolución de llamada.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// Nos permite cargar imágenes en un documento usando abreviaturas predefinidas, en lugar de URI.
/// Esto separará la lógica de carga de imágenes del resto de la construcción del documento.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Si esta devolución de llamada encuentra una de las taquigrafías de la imagen mientras se carga una imagen,
        // aplicará una lógica única para cada taquigrafía definida en lugar de tratarla como un URI.
        if (args.ResourceType == ResourceType.Image)
            switch (args.OriginalUri)
            {
                case "Google logo":
                    using (WebClient webClient = new WebClient())
                    {
                        args.SetData(webClient.DownloadData("http://www.google.com/images/logos/ps_logo2.png"));
                    }

                    return ResourceLoadingAction.UserProvided;

                case "Aspose logo":
                    args.SetData(File.ReadAllBytes(ImageDir + "Logo.jpg"));

                    return ResourceLoadingAction.UserProvided;

                case "Watermark":
                    args.SetData(File.ReadAllBytes(ImageDir + "Transparent background logo.png"));

                    return ResourceLoadingAction.UserProvided;
            }

        return ResourceLoadingAction.Default;
    }
}
```

### Ver también

* enum [ResourceLoadingAction](../../resourceloadingaction/)
* class [ResourceLoadingArgs](../../resourceloadingargs/)
* interface [IResourceLoadingCallback](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
