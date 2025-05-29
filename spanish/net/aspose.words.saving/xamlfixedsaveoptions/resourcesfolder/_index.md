---
title: XamlFixedSaveOptions.ResourcesFolder
linktitle: ResourcesFolder
articleTitle: ResourcesFolder
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad XamlFixedSaveOptions ResourcesFolder mejora las exportaciones de documentos al definir dónde se almacenan las imágenes y las fuentes en formato Xaml.
type: docs
weight: 30
url: /es/net/aspose.words.saving/xamlfixedsaveoptions/resourcesfolder/
---
## XamlFixedSaveOptions.ResourcesFolder property

Especifica la carpeta física donde se guardan los recursos (imágenes y fuentes) al exportar un documento al formato Xaml de página fija. El valor predeterminado es`nulo` .

```csharp
public string ResourcesFolder { get; set; }
```

## Observaciones

Cuando guardas un[`Document`](../../../aspose.words/document/) En el formato de página fija Xaml, Aspose.Words necesita guardar todas las imágenes incrustadas en el documento como archivos independientes.`ResourcesFolder` le permite especificar dónde se guardarán las imágenes y[`ResourcesFolderAlias`](../resourcesfolderalias/) permite especificar cómo se construirán las URI de las imágenes.

Si guarda un documento en un archivo y proporciona un nombre de archivo, Aspose.Words, de forma predeterminada, guarda las imágenes en la misma carpeta donde se guarda el archivo del documento. Utilice`ResourcesFolder` para anular este comportamiento.

Si guarda un documento en una secuencia, Aspose.Words no tiene una carpeta donde guardar las imágenes, pero aun así necesita guardarlas en algún lugar. En este caso, debe especificar una carpeta accesible mediante el comando`ResourcesFolder` propiedad

## Ejemplos

Muestra cómo imprimir las URI de los recursos vinculados creados al convertir un documento a formato fijo .xaml.

```csharp
public void ResourceFolder()
{
    Document doc = new Document(MyDir + "Rendering.docx");
    ResourceUriPrinter callback = new ResourceUriPrinter();

    // Crea un objeto "XamlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar la forma en que guardamos el documento en el formato de guardado XAML.
    XamlFixedSaveOptions options = new XamlFixedSaveOptions();

    Assert.AreEqual(SaveFormat.XamlFixed, options.SaveFormat);

    // Utilice la propiedad "ResourcesFolder" para asignar una carpeta en el sistema de archivos local a la que
    // Aspose.Words guardará todos los recursos vinculados del documento, como imágenes y fuentes.
    options.ResourcesFolder = ArtifactsDir + "XamlFixedResourceFolder";

    // Utilice la propiedad "ResourcesFolderAlias" para usar esta carpeta
    // al construir URI de imágenes en lugar del nombre de la carpeta de recursos.
    options.ResourcesFolderAlias = ArtifactsDir + "XamlFixedFolderAlias";

    options.ResourceSavingCallback = callback;

    // Una carpeta especificada por "ResourcesFolderAlias" deberá contener los recursos en lugar de "ResourcesFolder".
    // Debemos asegurarnos de que la carpeta exista antes de que los flujos de devolución de llamada puedan poner sus recursos en ella.
    Directory.CreateDirectory(options.ResourcesFolderAlias);

    doc.Save(ArtifactsDir + "XamlFixedSaveOptions.ResourceFolder.xaml", options);

    foreach (string resource in callback.Resources)
        Console.WriteLine(resource);
}

/// <summary>
/// Cuenta e imprime las URI de los recursos creados durante la conversión a .xaml fijo.
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
        // para redirigir cada flujo para colocar su recurso en la carpeta alias.
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
