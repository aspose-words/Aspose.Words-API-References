---
title: HtmlSaveOptions.CssStyleSheetFileName
linktitle: CssStyleSheetFileName
articleTitle: CssStyleSheetFileName
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad HtmlSaveOptions CssStyleSheetFileName personaliza sus exportaciones HTML con una ruta de archivo CSS específica, mejorando el estilo de su documento.
type: docs
weight: 50
url: /es/net/aspose.words.saving/htmlsaveoptions/cssstylesheetfilename/
---
## HtmlSaveOptions.CssStyleSheetFileName property

Especifica la ruta y el nombre del archivo de hoja de estilo en cascada (CSS) que se escribe cuando un documento se exporta a HTML. El valor predeterminado es una cadena vacía.

```csharp
public string CssStyleSheetFileName { get; set; }
```

## Observaciones

Esta propiedad solo tiene efecto cuando se guarda un documento en formato HTML y se solicita una hoja de estilo CSS externa mediante[`CssStyleSheetType`](../cssstylesheettype/).

Si esta propiedad está vacía, el archivo CSS se guardará en la misma carpeta y con el mismo nombre que el documento HTML pero con la extensión ".css".

Si solo se especifica la ruta pero no el nombre del archivo en esta propiedad, el archivo CSS se guardará en la carpeta especificada y tendrá el mismo nombre que el documento HTML pero con la extensión ".css".

Si la carpeta especificada por esta propiedad no existe, se creará automáticamente antes de guardar el archivo CSS .

Otra forma de especificar una carpeta donde se guarda el archivo CSS externo es usar[`ResourceFolder`](../resourcefolder/) .

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

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
