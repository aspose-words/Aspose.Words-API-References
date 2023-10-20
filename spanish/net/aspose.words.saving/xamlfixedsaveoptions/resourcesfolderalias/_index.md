---
title: XamlFixedSaveOptions.ResourcesFolderAlias
linktitle: ResourcesFolderAlias
articleTitle: ResourcesFolderAlias
second_title: Aspose.Words para .NET
description: XamlFixedSaveOptions ResourcesFolderAlias propiedad. Especifica el nombre de la carpeta utilizada para construir los URI de imagen escritos en un documento Xaml de página fija. El valor predeterminado esnulo  en C#.
type: docs
weight: 40
url: /es/net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolderalias/
---
## XamlFixedSaveOptions.ResourcesFolderAlias property

Especifica el nombre de la carpeta utilizada para construir los URI de imagen escritos en un documento Xaml de página fija. El valor predeterminado es`nulo` .

```csharp
public string ResourcesFolderAlias { get; set; }
```

## Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) en formato Xaml de página fija, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes.[`ResourcesFolder`](../resourcesfolder/) le permite especificar dónde se guardarán las imágenes y`ResourcesFolderAlias` permite especificar cómo se construirán los URI de la imagen.

## Ejemplos

Muestra cómo imprimir los URI de los recursos vinculados creados al convertir un documento a .xaml de formato fijo.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Crea un objeto "XamlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar cómo guardamos el documento en el formato de guardado XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Utilice la propiedad "ResourcesFolder" para asignar una carpeta en el sistema de archivos local en la que
    // Aspose.Words guardará todos los recursos vinculados del documento, como imágenes y fuentes.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Usa la propiedad "ResourcesFolderAlias" para usar esta carpeta
    // al construir URI de imágenes en lugar del nombre de la carpeta de recursos.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // Una carpeta especificada por "ResourcesFolderAlias" deberá contener los recursos en lugar de "ResourcesFolder".
    // Debemos asegurarnos de que la carpeta exista antes de que las transmisiones de la devolución de llamada puedan poner sus recursos en ella.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// Cuenta e imprime los URI de los recursos creados durante la conversión a .xaml fijo.
/// </summary>
private class ResourceUriPrinter : IResourceSavingCallback
{
    public ResourceUriPrinter()
    {
        Resources = new List<string>();
    }

    void IResourceSavingCallback.ResourceSaving(ResourceSavingArgs args)
    {
        Resources.Add($"Resource \"{args.ResourceFileName}\"\n\t{args.ResourceFileUri}");

        // Si especificamos un alias de carpeta de recursos, también necesitaríamos
        // para redirigir cada secuencia para colocar su recurso en la carpeta de alias.
        args.ResourceStream = new FileStream(args.ResourceFileUri, FileMode.Create);
        args.KeepResourceStreamOpen = false;
    }

    public List<string> Resources { get; }
}
```

### Ver también

* class [XamlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
