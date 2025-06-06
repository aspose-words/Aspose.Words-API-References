---
title: FontSavingArgs.IsSubsettingNeeded
linktitle: IsSubsettingNeeded
articleTitle: IsSubsettingNeeded
second_title: Aspose.Words para .NET
description: Descubra la propiedad FontSavingArgs IsSubsettingNeeded para controlar la subdivisión de fuentes y optimizar la exportación de recursos. ¡Mejore su flujo de trabajo de diseño hoy mismo!
type: docs
weight: 70
url: /es/net/aspose.words.saving/fontsavingargs/issubsettingneeded/
---
## FontSavingArgs.IsSubsettingNeeded property

Permite especificar si la fuente actual se creará un subconjunto antes de exportarla como un recurso de fuente.

```csharp
public bool IsSubsettingNeeded { get; set; }
```

## Observaciones

Las fuentes se pueden exportar como archivos de fuente originales completos o crear subconjuntos para incluir solo los caracteres utilizados en el documento. Crear subconjuntos permite reducir el tamaño de la fuente resultante.

De forma predeterminada, Aspose.Words decide si realizar un subconjunto o no comparando el tamaño del archivo de fuente original con el especificado en[`FontResourcesSubsettingSizeThreshold`](../../htmlsaveoptions/fontresourcessubsettingsizethreshold/) . Puede anular este comportamiento para fuentes individuales configurando el`IsSubsettingNeeded` propiedad.

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

* class [FontSavingArgs](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
