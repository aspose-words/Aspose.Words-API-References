---
title: FontSavingArgs.FontFileName
second_title: Referencia de API de Aspose.Words para .NET
description: FontSavingArgs propiedad. Obtiene o establece el nombre del archivo sin la ruta donde se guardará la fuente.
type: docs
weight: 40
url: /es/net/aspose.words.saving/fontsavingargs/fontfilename/
---
## FontSavingArgs.FontFileName property

Obtiene o establece el nombre del archivo (sin la ruta) donde se guardará la fuente.

```csharp
public string FontFileName { get; set; }
```

### Observaciones

Esta propiedad le permite redefinir cómo se generan los nombres de los archivos de fuentes durante la exportación a HTML.

Cuando se activa el evento, esta propiedad contiene el nombre de archivo que Aspose.Words generó . Puede cambiar el valor de esta propiedad para guardar la fuente en un archivo diferente. Tenga en cuenta que los nombres de los archivos deben ser únicos.

Aspose.Words genera automáticamente un nombre de archivo único para cada fuente incrustada al exportar a formato HTML. La forma en que se genera el nombre del archivo de fuente depende de si guarda el documento en un archivo o en una secuencia.

Al guardar un documento en un archivo, el nombre del archivo de fuente generado se ve como &lt;nombre del archivo base del documento&gt;.&lt;nombre del archivo original&gt;&lt;sufijo opcional&gt;.&lt;extensión&gt;.

Al guardar un documento en una secuencia, el nombre del archivo de fuente generado se parece a Aspose.Words.&lt;GUID del documento&gt;.&lt;nombre del archivo original&gt;&lt;sufijo opcional&gt;.&lt;extensión&gt;.

`FontFileName` debe contener solo el nombre del archivo sin la ruta. Aspose.Words determina la ruta para guardar usando el nombre del archivo del documento, el[`FontsFolder`](../../htmlsaveoptions/fontsfolder/) y [`FontsFolderAlias`](../../htmlsaveoptions/fontsfolderalias/) propiedades.

### Ejemplos

Muestra cómo definir una lógica personalizada para exportar fuentes al guardar en HTML.

```csharp
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Configure un objeto SaveOptions para exportar fuentes a archivos separados.
    // Establezca una devolución de llamada que manejará el guardado de fuentes de manera personalizada.
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

/// <summary>
/// Imprime información sobre las fuentes exportadas y las guarda en la misma carpeta del sistema local que su salida .html.
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

        // 2 - Guardarlo en una secuencia:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Ver también

* class [FontSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../fontsavingargs/)
* asamblea [Aspose.Words](../../../)


