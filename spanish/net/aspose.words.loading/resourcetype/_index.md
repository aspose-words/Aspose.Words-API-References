---
title: Enum ResourceType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Loading.ResourceType enumeración. Tipo de recurso cargado.
type: docs
weight: 3500
url: /es/net/aspose.words.loading/resourcetype/
---
## ResourceType enumeration

Tipo de recurso cargado.

```csharp
public enum ResourceType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Image | `0` | Imagen. |
| CssStyleSheet | `1` | hoja de estilo Css. |
| Document | `2` | Documento. |

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


