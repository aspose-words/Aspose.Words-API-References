---
title: ResourceLoadingArgs Class
linktitle: ResourceLoadingArgs
articleTitle: ResourceLoadingArgs
second_title: Aspose.Words para .NET
description: Descubra la clase Aspose.Words.Loading.ResourceLoadingArgs, diseñada para optimizar la carga de recursos en sus aplicaciones. ¡Descubra una integración fluida hoy mismo!
type: docs
weight: 4150
url: /es/net/aspose.words.loading/resourceloadingargs/
---
## ResourceLoadingArgs class

Proporciona datos para el[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) método.

```csharp
public class ResourceLoadingArgs
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [OriginalUri](../../aspose.words.loading/resourceloadingargs/originaluri/) { get; } | URI original del recurso tal como se especifica en el documento importado. |
| [ResourceType](../../aspose.words.loading/resourceloadingargs/resourcetype/) { get; } | Tipo de recurso. |
| [Uri](../../aspose.words.loading/resourceloadingargs/uri/) { get; set; } | URI del recurso que se utiliza para la descarga si[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) regresaDefault. |

## Métodos

| Nombre | Descripción |
| --- | --- |
| [SetData](../../aspose.words.loading/resourceloadingargs/setdata/)(*byte[]*) | Establece los datos proporcionados por el usuario del recurso que se utiliza si[`ResourceLoading`](../iresourceloadingcallback/resourceloading/) regresaUserProvided . |

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

* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)
