---
title: IPageSavingCallback.PageSaving
linktitle: PageSaving
articleTitle: PageSaving
second_title: Aspose.Words para .NET
description: Descubra el método iPageSavingCallback en Aspose.Words, diseñado para optimizar el guardado de páginas en formatos fijos. ¡Mejore su gestión documental hoy mismo!
type: docs
weight: 10
url: /es/net/aspose.words.saving/ipagesavingcallback/pagesaving/
---
## IPageSavingCallback.PageSaving method

Se llama cuando Aspose.Words guarda una página separada en formatos de página fijos.

```csharp
public void PageSaving(PageSavingArgs args)
```

## Ejemplos

Muestra cómo utilizar una devolución de llamada para guardar un documento en HTML página por página.

```csharp
public void PageFileNames()
{
    Document doc = new Document();
    DocumentBuilder builder = new DocumentBuilder(doc);

    builder.Writeln("Page 1.");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 2.");
    builder.InsertImage(ImageDir + "Logo.jpg");
    builder.InsertBreak(BreakType.PageBreak);
    builder.Writeln("Page 3.");

    // Crea un objeto "HtmlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar la forma en que convertimos el documento a HTML.
    HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions();

    // Guardaremos cada página de este documento en un archivo HTML separado en el sistema de archivos local.
    // Establezca una devolución de llamada que nos permita nombrar cada documento HTML de salida.
    htmlFixedSaveOptions.PageSavingCallback = new CustomFileNamePageSavingCallback();

    doc.Save(ArtifactsDir + "SavingCallback.PageFileNames.html", htmlFixedSaveOptions);

    string[] filePaths = Directory.GetFiles(ArtifactsDir).Where(
        s => s.StartsWith(ArtifactsDir + "SavingCallback.PageFileNames.Page_")).OrderBy(s => s).ToArray();

    Assert.AreEqual(3, filePaths.Length);
}

/// <summary>
/// Guarda todas las páginas en un archivo y directorio especificado dentro.
/// </summary>
private class CustomFileNamePageSavingCallback : IPageSavingCallback
{
    public void PageSaving(PageSavingArgs args)
    {
        string outFileName = $"{ArtifactsDir}SavingCallback.PageFileNames.Page_{args.PageIndex}.html";

        // A continuación se muestran dos formas de especificar dónde Aspose.Words guardará cada página del documento.
        // 1 - Establezca un nombre de archivo para el archivo de página de salida:
        args.PageFileName = outFileName;

        // 2 - Crea una secuencia personalizada para el archivo de página de salida:
        args.PageStream = new FileStream(outFileName, FileMode.Create);

        Assert.False(args.KeepPageStreamOpen);
    }
}
```

### Ver también

* class [PageSavingArgs](../../pagesavingargs/)
* interface [IPageSavingCallback](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
