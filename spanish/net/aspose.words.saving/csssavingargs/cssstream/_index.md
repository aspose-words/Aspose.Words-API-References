---
title: CssSavingArgs.CssStream
linktitle: CssStream
articleTitle: CssStream
second_title: Aspose.Words para .NET
description: CssSavingArgs CssStream propiedad. Permite especificar la secuencia donde se guardará la información CSS en C#.
type: docs
weight: 10
url: /es/net/aspose.words.saving/csssavingargs/cssstream/
---
## CssSavingArgs.CssStream property

Permite especificar la secuencia donde se guardará la información CSS.

```csharp
public Stream CssStream { get; set; }
```

## Observaciones

Esta propiedad le permite guardar información CSS en una secuencia.

El valor predeterminado es`nulo` . Esta propiedad no impide guardar información CSS en un archivo ni incrustarla en un documento HTML. Para suprimir la exportación de CSS utilice el[`IsExportNeeded`](../isexportneeded/) propiedad.

Usando[`ICssSavingCallback`](../../icsssavingcallback/) no puedes sustituir CSS por otro. Está destinado únicamente a guardar CSS en una secuencia.

## Ejemplos

Muestra cómo trabajar con hojas de estilo CSS que crea una conversión HTML.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Crea un objeto "HtmlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar cómo convertimos el documento a HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Establece la propiedad "CssStylesheetType" en "CssStyleSheetType.External" para
    // acompaña un documento HTML guardado con un archivo de hoja de estilo CSS externo.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // A continuación se muestran dos formas de especificar directorios y nombres de archivos para las hojas de estilo CSS de salida.
    // 1 - Usa la propiedad "CssStyleSheetFileName" para asignar un nombre de archivo a nuestra hoja de estilo:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Usa una devolución de llamada personalizada para nombrar nuestra hoja de estilo:
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
        // Podemos acceder al documento fuente completo a través de la propiedad "Documento".
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

* class [CssSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
