---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlFixedSaveOptions propiedad. Especifica si las fuentes se deben incrustar en el documento HTML en formato Base64. Tenga en cuenta que establecer este indicador puede aumentar significativamente el tamaño del archivo HTML de salida.
type: docs
weight: 50
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

Especifica si las fuentes se deben incrustar en el documento HTML en formato Base64. Tenga en cuenta que establecer este indicador puede aumentar significativamente el tamaño del archivo HTML de salida.

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

### Ejemplos

Muestra cómo determinar dónde almacenar las fuentes incrustadas al exportar un documento a Html.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// Cuando exportamos un documento con fuentes incrustadas a .html,
// Aspose.Words puede colocar las fuentes en dos ubicaciones posibles.
// Establecer el indicador "ExportEmbeddedFonts" en "true" almacenará los datos sin procesar para las fuentes incrustadas dentro de la hoja de estilo CSS,
// en la propiedad "url" de la regla "@font-face". Esto puede crear un enorme archivo de hoja de estilos CSS
// y reduzca la cantidad de archivos externos que creará esta conversión de HTML.
// Establecer este indicador en "falso" creará un archivo para cada fuente.
// La hoja de estilo CSS vinculará a cada archivo de fuente usando la propiedad "url" de la regla "@font-face".
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedFonts = exportEmbeddedFonts
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts/styles.css");

if (exportEmbeddedFonts)
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(].+[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(0, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], url[(]'font001[.]woff'[)] format[(]'woff'[)]; }").Success);
    Assert.AreEqual(2, Directory.GetFiles(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedFonts").Count(f => f.EndsWith(".woff")));
}
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* asamblea [Aspose.Words](../../../)


