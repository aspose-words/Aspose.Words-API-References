---
title: ResourceLoadingArgs.SetData
linktitle: SetData
articleTitle: SetData
second_title: Aspose.Words para .NET
description: Descubra cómo el método ResourceLoadingArgs SetData mejora la experiencia del usuario al administrar de manera eficiente los datos de recursos para un rendimiento óptimo.
type: docs
weight: 40
url: /es/net/aspose.words.loading/resourceloadingargs/setdata/
---
## ResourceLoadingArgs.SetData method

Establece los datos proporcionados por el usuario del recurso que se utiliza si[`ResourceLoading`](../../iresourceloadingcallback/resourceloading/) regresaUserProvided .

```csharp
public void SetData(byte[] data)
```

## Ejemplos

Muestra cómo personalizar el proceso de carga de recursos externos en un documento.

```csharp
public void ResourceLoadingCallback()
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Las imágenes generalmente se insertan utilizando una URI o una matriz de bytes.
    // Cada instancia de una carga de recursos llamará al método ResourceLoading de nuestra devolución de llamada.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");
}

/// <summary>
/// Nos permite cargar imágenes en un documento utilizando abreviaturas predefinidas, en lugar de URI.
/// Esto separará la lógica de carga de imágenes del resto de la construcción del documento.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Si esta devolución de llamada encuentra una de las abreviaturas de imagen al cargar una imagen,
        // aplicará una lógica única para cada abreviatura definida en lugar de tratarla como una URI.
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

* class [ResourceLoadingArgs](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
