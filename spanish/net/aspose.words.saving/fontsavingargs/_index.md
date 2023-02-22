---
title: Class FontSavingArgs
second_title: Referencia de API de Aspose.Words para .NET
description: Aspose.Words.Saving.FontSavingArgs clase. Proporciona datos para elFontSaving evento.
type: docs
weight: 4770
url: /es/net/aspose.words.saving/fontsavingargs/
---
## FontSavingArgs class

Proporciona datos para el[`FontSaving`](../ifontsavingcallback/fontsaving/) evento.

```csharp
public class FontSavingArgs
```

## Propiedades

| Nombre | Descripción |
| --- | --- |
| [Bold](../../aspose.words.saving/fontsavingargs/bold/) { get; } | Indica si la fuente actual está en negrita. |
| [Document](../../aspose.words.saving/fontsavingargs/document/) { get; } | Obtiene el objeto de documento que se está guardando. |
| [FontFamilyName](../../aspose.words.saving/fontsavingargs/fontfamilyname/) { get; } | Indica el nombre de la familia de fuentes actual. |
| [FontFileName](../../aspose.words.saving/fontsavingargs/fontfilename/) { get; set; } | Obtiene o establece el nombre del archivo (sin la ruta) donde se guardará la fuente. |
| [FontStream](../../aspose.words.saving/fontsavingargs/fontstream/) { get; set; } | Permite especificar el flujo donde se guardará la fuente. |
| [IsExportNeeded](../../aspose.words.saving/fontsavingargs/isexportneeded/) { get; set; } | Permite especificar si la fuente actual se exportará como recurso de fuente. El valor predeterminado es`verdadero` . |
| [IsSubsettingNeeded](../../aspose.words.saving/fontsavingargs/issubsettingneeded/) { get; set; } | Permite especificar si la fuente actual será un subconjunto antes de exportar como recurso de fuente. |
| [Italic](../../aspose.words.saving/fontsavingargs/italic/) { get; } | Indica si la fuente actual es cursiva. |
| [KeepFontStreamOpen](../../aspose.words.saving/fontsavingargs/keepfontstreamopen/) { get; set; } | Especifica si Aspose.Words debe mantener la transmisión abierta o cerrarla después de guardar una fuente. |
| [OriginalFileName](../../aspose.words.saving/fontsavingargs/originalfilename/) { get; } | Obtiene el nombre del archivo de fuente original con una extensión. |
| [OriginalFileSize](../../aspose.words.saving/fontsavingargs/originalfilesize/) { get; } | Obtiene el tamaño de archivo de fuente original. |

### Observaciones

Cuando Aspose.Words guarda un documento en HTML o formatos relacionados y[`ExportFontResources`](../htmlsaveoptions/exportfontresources/) se establece en **verdadero**, guarda cada tema de fuente para exportarlo en un archivo separado.

`FontSavingArgs` controla si se debe exportar un recurso de fuente en particular y cómo.

`FontSavingArgs`también permite redefinir cómo se generan los nombres de los archivos de fuentes o eludir por completo el almacenamiento de fuentes en archivos proporcionando sus propios objetos de flujo.

Para decidir si desea guardar un recurso de fuente en particular, use el[`IsExportNeeded`](./isexportneeded/) propiedad.

Para guardar fuentes en secuencias en lugar de archivos, use el[`FontStream`](./fontstream/) propiedad.

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

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)


