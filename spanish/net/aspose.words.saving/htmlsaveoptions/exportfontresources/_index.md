---
title: HtmlSaveOptions.ExportFontResources
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlSaveOptions propiedad. Especifica si los recursos de fuentes deben exportarse a HTML MHTML o EPUB. El valor predeterminado esFALSO .
type: docs
weight: 140
url: /es/net/aspose.words.saving/htmlsaveoptions/exportfontresources/
---
## HtmlSaveOptions.ExportFontResources property

Especifica si los recursos de fuentes deben exportarse a HTML, MHTML o EPUB. El valor predeterminado es`FALSO` .

```csharp
public bool ExportFontResources { get; set; }
```

### Observaciones

La exportación de recursos de fuentes permite una representación consistente del documento independientemente de las fuentes disponibles en el entorno de un usuario determinado.

Si`ExportFontResources` se establece en`verdadero` , el documento HTML principal hará referencia a cada fuente a través de el CSS 3 **@Perfil delantero** at-rule y las fuentes se generarán como archivos separados. Al exportar a formatos IDPF EPUB o MHTML , las fuentes se incrustarán en el paquete correspondiente junto con otros archivos subsidiarios.

Si[`ExportFontsAsBase64`](../exportfontsasbase64/) se establece en`verdadero` las fuentes no se guardarán en archivos separados. En su lugar, se incrustarán en **@Perfil delantero** reglas at en codificación Base64.

**¡Importante!** Al exportar recursos de fuentes, se deben considerar cuestiones de licencia de fuentes. Los autores que deseen utilizar fuentes específicas a través de un mecanismo de fuente descargable siempre deben verificar cuidadosamente que el uso previsto esté dentro del alcance de la licencia de fuente. Actualmente, muchas fuentes comerciales no permiten la descarga web de sus fuentes en ningún formato. Los acuerdos de licencia que cubren algunas fuentes señalan específicamente que el uso a través de **@Perfil delantero** Rules en hojas de estilo CSS no está permitido. El subconjunto de fuentes también puede violar los términos de la licencia.

### Ejemplos

Muestra cómo definir una lógica personalizada para exportar fuentes al guardar en HTML.

```csharp
public void SaveExportedFonts()
{
    Document doc = new Document(MyDir + "Rendering.docx");

    // Configurar un objeto SaveOptions para exportar fuentes a archivos separados.
    // Establece una devolución de llamada que manejará el guardado de fuentes de forma personalizada.
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

        // 2 - Guárdalo en una secuencia:
        args.FontStream =
            new FileStream(ArtifactsDir + args.OriginalFileName.Split(Path.DirectorySeparatorChar).Last(), FileMode.Create);
        Assert.False(args.KeepFontStreamOpen);
    }
}
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlsaveoptions/)
* asamblea [Aspose.Words](../../../)


