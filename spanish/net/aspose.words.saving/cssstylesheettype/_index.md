---
title: Enum CssStyleSheetType
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.CssStyleSheetType enumeración. Especifica cómo se exportan los estilos CSS hoja de estilo en cascada a HTML.
type: docs
weight: 4630
url: /es/net/aspose.words.saving/cssstylesheettype/
---
## CssStyleSheetType enumeration

Especifica cómo se exportan los estilos CSS (hoja de estilo en cascada) a HTML.

```csharp
public enum CssStyleSheetType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Inline | `0` | Los estilos CSS se escriben en línea (como un valor de la **estilo** atributo en cada elemento). |
| Embedded | `1` | Los estilos CSS se escriben por separado del contenido en una hoja de estilo incrustada en el archivo HTML. |
| External | `2` | Los estilos CSS se escriben por separado del contenido de una hoja de estilo en un archivo externo. El archivo HTML vincula la hoja de estilo. |

### Ejemplos

Muestra cómo trabajar con hojas de estilo CSS que crea una conversión HTML.

```csharp
public void ExternalCssFilenames()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Crear un objeto "HtmlFixedSaveOptions", que podemos pasar al método "Guardar" del documento
    // para modificar cómo convertimos el documento a HTML.
    HtmlSaveOptions options = new HtmlSaveOptions();

    // Establecer la propiedad "CssStylesheetType" en "CssStyleSheetType.External" para
    // acompañar un documento HTML guardado con un archivo de hoja de estilo CSS externo.
    options.CssStyleSheetType = CssStyleSheetType.External;

    // A continuación se muestran dos formas de especificar directorios y nombres de archivo para las hojas de estilo CSS de salida.
    // 1 - Usa la propiedad "CssStyleSheetFileName" para asignar un nombre de archivo a nuestra hoja de estilo:
    options.CssStyleSheetFileName = ArtifactsDir + "SavingCallback.ExternalCssFilenames.css";

    // 2 - Use una devolución de llamada personalizada para nombrar nuestra hoja de estilo:
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
        // Podemos acceder a todo el documento de origen a través de la propiedad "Documento".
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

* property [CssStyleSheetType](../htmlsaveoptions/cssstylesheettype/)
* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


