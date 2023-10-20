---
title: CssSavingArgs Class
linktitle: CssSavingArgs
articleTitle: CssSavingArgs
second_title: Aspose.Words para .NET
description: Aspose.Words.Saving.CssSavingArgs clase. Proporciona datos para elCssSaving evento en C#.
type: docs
weight: 4880
url: /es/net/aspose.words.saving/csssavingargs/
---
## CssSavingArgs class

Proporciona datos para el[`CssSaving`](../icsssavingcallback/csssaving/) evento.

Para obtener más información, visite el[Guardar un documento](https://docs.aspose.com/words/net/save-a-document/) artículo de documentación.

```csharp
public class CssSavingArgs
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [CssStream](../../aspose.words.saving/csssavingargs/cssstream/) { get; set; } | Permite especificar la secuencia donde se guardará la información CSS. |
| [Document](../../aspose.words.saving/csssavingargs/document/) { get; } | Obtiene el objeto del documento que se está guardando actualmente. |
| [IsExportNeeded](../../aspose.words.saving/csssavingargs/isexportneeded/) { get; set; } | Permite especificar si el CSS se exportará a un archivo y se incrustará en un documento HTML. El valor predeterminado es`verdadero` . Cuando esta propiedad es`FALSO` , la información CSS no se guardará en un archivo CSS y no se incrustará en el documento HTML. |
| [KeepCssStreamOpen](../../aspose.words.saving/csssavingargs/keepcssstreamopen/) { get; set; } | Especifica si Aspose.Words debe mantener la secuencia abierta o cerrarla después de guardar una información CSS. |

## Observaciones

De forma predeterminada, cuando Aspose.Words guarda un documento en HTML, guarda la información CSS inline (como un valor del**estilo** atributo en cada elemento).

`CssSavingArgs`permite guardar información CSS en un archivo proporcionando su propio objeto de flujo.

Para guardar CSS en la secuencia, use el[`CssStream`](./cssstream/) propiedad.

Para evitar guardar CSS en un archivo e incrustarlo en un documento HTML, utilice el[`IsExportNeeded`](./isexportneeded/) propiedad.

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
