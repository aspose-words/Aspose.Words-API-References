---
title: Enum ResourceLoadingAction
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Loading.ResourceLoadingAction enumeración. Especifica el modo de carga de recursos.
type: docs
weight: 3480
url: /es/net/aspose.words.loading/resourceloadingaction/
---
## ResourceLoadingAction enumeration

Especifica el modo de carga de recursos.

```csharp
public enum ResourceLoadingAction
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Default | `0` | Aspose.Words cargará este recurso como de costumbre. |
| Skip | `1` | Aspose.Words omitirá la carga de este recurso. Solo se almacenará el enlace sin datos para una imagen, la hoja de estilo CSS se ignorará para el formato HTML. |
| UserProvided | `2` | Aspose.Words utilizará la matriz de bytes proporcionada por el usuario en[`SetData`](../resourceloadingargs/setdata/) como datos de recursos. |

### Ejemplos

Muestra cómo personalizar el proceso de carga de recursos externos en un documento.

```csharp
{
    Document doc = new Document();
    doc.ResourceLoadingCallback = new ImageNameHandler();

    DocumentBuilder builder = new DocumentBuilder(doc);

    // Las imágenes generalmente se insertan usando un URI o una matriz de bytes.
    // Cada instancia de una carga de recursos llamará al método ResourceLoading de nuestra devolución de llamada.
    builder.InsertImage("Google logo");
    builder.InsertImage("Aspose logo");
    builder.InsertImage("Watermark");

    Assert.AreEqual(3, doc.GetChildNodes(NodeType.Shape, true).Count);

    doc.Save(ArtifactsDir + "DocumentBase.ResourceLoadingCallback.docx");

/// <summary>
/// Nos permite cargar imágenes en un documento utilizando abreviaturas predefinidas, en lugar de URI.
/// Esto separará la lógica de carga de imágenes del resto de la construcción del documento.
/// </summary>
private class ImageNameHandler : IResourceLoadingCallback
{
    public ResourceLoadingAction ResourceLoading(ResourceLoadingArgs args)
    {
        // Si esta devolución de llamada encuentra una de las abreviaturas de imagen al cargar una imagen,
        // aplicará una lógica única para cada abreviatura definida en lugar de tratarlo como un URI.
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


