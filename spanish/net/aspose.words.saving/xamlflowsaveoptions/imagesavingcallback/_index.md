---
title: XamlFlowSaveOptions.ImageSavingCallback
second_title: Referencia de API de Aspose.Words para .NET
description: XamlFlowSaveOptions propiedad. Permite controlar cómo se guardan las imágenes cuando un documento se guarda en XAML.
type: docs
weight: 20
url: /es/net/aspose.words.saving/xamlflowsaveoptions/imagesavingcallback/
---
## XamlFlowSaveOptions.ImageSavingCallback property

Permite controlar cómo se guardan las imágenes cuando un documento se guarda en XAML.

```csharp
public IImageSavingCallback ImageSavingCallback { get; set; }
```

### Ejemplos

Muestra cómo imprimir los nombres de archivo de las imágenes vinculadas creadas al convertir un documento a .xaml de formato de flujo.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    ImageUriPrinter callback = new ImageUriPrinter(ArtifactsDir + "XamlFlowImageFolderAlias");

    // Crear un objeto "XamlFlowSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar cómo guardamos el documento en el formato de guardado XAML.
    XamlFlowSaveOptions options = new XamlFlowSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFlow, options.SaveFormat);

    // Utilice la propiedad "ImagesFolder" para asignar una carpeta en el sistema de archivos local en la que
    // Aspose.Words guardará todas las imágenes vinculadas del documento.
    options.ImagesFolder = ArtifactsDir + "XamlFlowImageFolder";

    // Usa la propiedad "ImagesFolderAlias" para usar esta carpeta
    // al construir URI de imágenes en lugar del nombre de la carpeta de imágenes.
    options.ImagesFolderAlias = ArtifactsDir + "XamlFlowImageFolderAlias";

    options.ImageSavingCallback = callback;

    // Una carpeta especificada por "ImagesFolderAlias" deberá contener los recursos en lugar de "ImagesFolder".
    // Debemos asegurarnos de que la carpeta exista antes de que los flujos de devolución de llamada puedan poner sus recursos en ella.
    Directory.CreateDirectory(options.ImagesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFlowSaveOptions.ImageFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine($"{callback.ImagesFolderAlias}/{resource}");

/// <summary>
/// Cuenta e imprime los nombres de archivo de las imágenes mientras su documento principal se convierte a formato de flujo .xaml.
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

        // Si especificamos un alias de carpeta de imágenes, también necesitaríamos
        // para redirigir cada transmisión para colocar su imagen en la carpeta de alias.
        args.ImageStream = new FileStream($"{ImagesFolderAlias}/{args.ImageFileName}", FileMode.Create);
        args.KeepImageStreamOpen = false;
    }

    public string ImagesFolderAlias { get; }
    public List<string> Resources { get; }
}
```

### Ver también

* interface [IImageSavingCallback](../../iimagesavingcallback/)
* class [XamlFlowSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../xamlflowsaveoptions/)
* asamblea [Aspose.Words](../../../)


