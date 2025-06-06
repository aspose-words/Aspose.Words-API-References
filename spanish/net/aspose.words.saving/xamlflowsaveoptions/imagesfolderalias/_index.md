---
title: XamlFlowSaveOptions.ImagesFolderAlias
linktitle: ImagesFolderAlias
articleTitle: ImagesFolderAlias
second_title: Aspose.Words para .NET
description: Descubre la propiedad ImagesFolderAlias de XamlFlowSaveOptions para personalizar las rutas URI de imágenes en documentos XAML. ¡Mejora tus proyectos fácilmente!
type: docs
weight: 40
url: /es/net/aspose.words.saving/xamlflowsaveoptions/imagesfolderalias/
---
## XamlFlowSaveOptions.ImagesFolderAlias property

Especifica el nombre de la carpeta utilizada para construir las URI de imágenes escritas en un documento XAML. El valor predeterminado es una cadena vacía.

```csharp
public string ImagesFolderAlias { get; set; }
```

## Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) en formato XAML, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes.[`ImagesFolder`](../imagesfolder/) le permite especificar dónde se guardarán las imágenes y`ImagesFolderAlias` permite especificar cómo se construirán las URI de las imágenes.

Si`ImagesFolderAlias` no es una cadena vacía, entonces la URI de la imagen escrita en XAML seráImagesFolderAlias + &lt;nombre del archivo de imagen&gt;.

Si`ImagesFolderAlias` es una cadena vacía, entonces la URI de la imagen escrita en XAML seráImagesFolder + &lt;nombre del archivo de imagen&gt;.

Si`ImagesFolderAlias` se establece en '.' (punto), entonces el nombre del archivo de imagen se escribirá en XAML sin ruta, independientemente de otras opciones.

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
