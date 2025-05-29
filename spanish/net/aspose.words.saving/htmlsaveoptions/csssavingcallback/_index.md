---
title: HtmlSaveOptions.CssSavingCallback
linktitle: CssSavingCallback
articleTitle: CssSavingCallback
second_title: Aspose.Words para .NET
description: Controla el guardado de estilos CSS con HtmlSaveOptions CssSavingCallback. Optimiza la exportación de tus documentos a HTML, MHTML o EPUB sin esfuerzo.
type: docs
weight: 40
url: /es/net/aspose.words.saving/htmlsaveoptions/csssavingcallback/
---
## HtmlSaveOptions.CssSavingCallback property

Permite controlar cómo se guardan los estilos CSS cuando un documento se guarda en HTML, MHTML o EPUB.

```csharp
public ICssSavingCallback CssSavingCallback { get; set; }
```

## Ejemplos

Muestra cómo trabajar con hojas de estilo CSS que crea una conversión HTML.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Crea un objeto "HtmlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar la forma en que convertimos el documento a HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Establezca la propiedad "CssStylesheetType" en "CssStyleSheetType.External" para
    // Acompañe un documento HTML guardado con un archivo de hoja de estilo CSS externo.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // A continuación se muestran dos formas de especificar directorios y nombres de archivos para las hojas de estilo CSS de salida.
    // 1 - Utilice la propiedad "CssStyleSheetFileName" para asignar un nombre de archivo a nuestra hoja de estilo:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Utilice una devolución de llamada personalizada para nombrar nuestra hoja de estilo:
    options.CssSavingCallback =
        new CustomCssSavingCallback(ArtifactsDir + "SavingCallback.ExternalCssFilenames.css", true, false);

    doc.Save(ArtifactsDir + "SavingCallback.ExternalCssFilenames.html", options);
}

/// <summary>
/// Establece un nombre de archivo personalizado, junto con otros parámetros para una hoja de estilo CSS externa.
/// </summary>
private class CustomCssSavingCallback : ICssSavingCallback
{
    public CustomCssSavingCallback(string cssDocFilename, bool isExportNeeded, bool keepCssStreamOpen)
    {
        mCssTextFileName = cssDocFilename;
        mIsExportNeeded = isExportNeeded;
        mKeepCssStreamOpen = keepCssStreamOpen;
    }

    public void CssSaving(CssSavingArgs args)
    {
        //Podemos acceder al documento fuente completo a través de la propiedad "Documento".
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        args.CssStream = new FileStream(mCssTextFileName, FileMode.Create);
        args.IsExportNeeded = mIsExportNeeded;
        args.KeepCssStreamOpen = mKeepCssStreamOpen;

        Assert.True(args.CssStream.CanWrite);
    }

    private readonly string mCssTextFileName;
    private readonly bool mIsExportNeeded;
    private readonly bool mKeepCssStreamOpen;
}
```

### Ver también

* interface [ICssSavingCallback](../../icsssavingcallback/)
* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
