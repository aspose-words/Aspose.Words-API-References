---
title: XamlFlowSaveOptions.ImagesFolder
linktitle: ImagesFolder
articleTitle: ImagesFolder
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ImagesFolder de XamlFlowSaveOptions le permite especificar fácilmente una carpeta para guardar imágenes al exportar documentos al formato XAML.
type: docs
weight: 30
url: /es/net/aspose.words.saving/xamlflowsaveoptions/imagesfolder/
---
## XamlFlowSaveOptions.ImagesFolder property

Especifica la carpeta física donde se guardan las imágenes al exportar un documento al formato XAML. El valor predeterminado es una cadena vacía.

```csharp
public string ImagesFolder { get; set; }
```

## Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) en formato XAML, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes.`ImagesFolder` le permite especificar dónde se guardarán las imágenes y[`ImagesFolderAlias`](../imagesfolderalias/) permite especificar cómo se construirán las URI de las imágenes.

Si guarda un documento en un archivo y proporciona un nombre de archivo, Aspose.Words, de forma predeterminada, guarda las imágenes en la misma carpeta donde se guarda el archivo del documento. Usar`ImagesFolder` para anular este comportamiento.

Si guarda un documento en una secuencia, Aspose.Words no tiene una carpeta donde guardar las imágenes, , pero aun así necesita guardarlas en algún lugar. En este caso, debe especificar una carpeta accesible en el`ImagesFolder` propiedad o proporcionar secuencias personalizadas a través de [`ImageSavingCallback`](../imagesavingcallback/) controlador de eventos.

## Ejemplos

Muestra cómo imprimir los nombres de archivos de imágenes vinculadas creadas al convertir un documento a formato de flujo .xaml.

```csharp
public void ImageFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Crea un objeto "XamlFlowSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar la forma en que guardamos el documento en el formato de guardado XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Utilice la propiedad "ImagesFolder" para asignar una carpeta en el sistema de archivos local en la que
    // Aspose.Words guardará todas las imágenes vinculadas del documento.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Utilice la propiedad "ImagesFolderAlias" para usar esta carpeta
    // al construir URI de imágenes en lugar del nombre de la carpeta de imágenes.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Una carpeta especificada por "ImagesFolderAlias" deberá contener los recursos en lugar de "ImagesFolder".
    // Debemos asegurarnos de que la carpeta exista antes de que los flujos de devolución de llamada puedan poner sus recursos en ella.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");
}

/// <summary>
/// Cuenta e imprime nombres de archivos de imágenes mientras su documento principal se convierte a formato de flujo .xaml.
/// </summary>
private class ImageUriPrinter : IImageSavingCallback
{
    public ImageUriPrinter(string imagesFolderAlias)
    {
        ImagesFolderAlias = imagesFolderAlias;
        Resources = new List<string>();
    }

    void IImageSavingCallback.ImageSaving(ImageSavingArgs args)
    {
        Resources.Add(args.ImageFileName);

        // Si especificamos un alias de carpeta de imágenes, también lo necesitaríamos
        // para redirigir cada transmisión para colocar su imagen en la carpeta de alias.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Ver también

* class [XamlFlowSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
