---
title: HtmlSaveOptions.ExportFontResources
linktitle: ExportFontResources
articleTitle: ExportFontResources
second_title: Aspose.Words para .NET
description: Descubra la propiedad HtmlSaveOptions ExportFontResources para controlar la exportación de fuentes para HTML, MHTML o EPUB. ¡Maximice el atractivo visual de su documento!
type: docs
weight: 140
url: /es/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Especifica si los recursos de fuentes deben exportarse a HTML, MHTML o EPUB. El valor predeterminado es`FALSO` .

```csharp
public bool ExportFontResources { get; set; }
```

## Observaciones

La exportación de recursos de fuentes permite una representación consistente de los documentos independientemente de las fuentes disponibles en el entorno de un usuario determinado.

Si`ExportFontResources` está configurado para`verdadero` , el documento HTML principal hará referencia a cada fuente a través de el CSS 3**@font-face** La regla at y las fuentes se generarán como archivos separados. Al exportar a formatos IDPF EPUB o MHTML , las fuentes se integrarán en el paquete correspondiente junto con otros archivos secundarios.

Si[`ExportFontsAsBase64`](../exportfontsasbase64/) está configurado para`verdadero` , las fuentes no se guardarán en archivos separados. En su lugar, se incrustarán en**@font-face** reglas at en codificación Base64.

**¡Importante!**Al exportar recursos de fuentes, se deben considerar las cuestiones de licencias de fuentes. Los autores que deseen usar fuentes específicas mediante un mecanismo de fuentes descargables deben verificar cuidadosamente que el uso previsto esté dentro del alcance de la licencia de la fuente. Actualmente, muchas fuentes comerciales no permiten la descarga web de sus fuentes en ningún formato. Los acuerdos de licencia que cubren algunas fuentes especifican que el uso mediante**@font-face** rules no está permitido en hojas de estilo CSS. La subdivisión de fuentes también puede infringir los términos de la licencia.

## Ejemplos

Muestra cómo definir lógica personalizada para exportar fuentes al guardar en HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Configure un objeto SaveOptions para exportar fuentes a archivos separados.
    // Establezca una devolución de llamada que manejará el guardado de fuentes de una manera personalizada.
    HtmlSaveOptions options = new HtmlSaveOptions
    {
        ExportFontResources = true,
        FontSavingCallback = new HandleFontSaving()
    };

    // La devolución de llamada exportará archivos .ttf y los guardará junto con el documento de salida.
    doc.Save(ArtifactsDir + "HtmlSaveOptions.SaveExportedFonts.html", options);

    foreach (string fontFilename in Array.FindAll(Directory.GetFiles(ArtifactsDir), s => s.EndsWith(".ttf")))
    {
        Console.WriteLine(fontFilename);
    }

}

/// <summary>
/// Imprime información sobre las fuentes exportadas y las guarda en la misma carpeta del sistema local que su archivo .html de salida.
/// </summary>
public class HandleFontSaving : IFontSavingCallback
{
    void IFontSavingCallback.FontSaving(FontSavingArgs args)
    {
        Console.Write($"Font:\t{args.FontFamilyName}");
        if (args.Bold) Console.Write(", bold");
        if (args.Italic) Console.Write(", italic");
        Console.WriteLine($"\nSource:\t{args.OriginalFileName}, {args.OriginalFileSize} bytes\n");

        // También podemos acceder al documento fuente desde aquí.
        Assert.True(args.Document.OriginalFileName.EndsWith("Rendering.docx"));

        Assert.True(args.IsExportNeeded);
        Assert.True(args.IsSubsettingNeeded);

        // Hay dos formas de guardar una fuente exportada.
        // 1 - Guárdelo en una ubicación del sistema de archivos local:
        args.FontFileName = args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last();

        // 2 - Guárdalo en una secuencia:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
