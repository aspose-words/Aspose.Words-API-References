---
title: HtmlFixedSaveOptions.ExportEmbeddedFonts
linktitle: ExportEmbeddedFonts
articleTitle: ExportEmbeddedFonts
second_title: Aspose.Words para .NET
description: Controle la incrustación de fuentes en su HTML con la propiedad ExportEmbeddedFonts. Mejore la calidad del documento y administre eficazmente el tamaño del archivo.
type: docs
weight: 50
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedfonts/
---
## HtmlFixedSaveOptions.ExportEmbeddedFonts property

Especifica si las fuentes deben incrustarse en el documento HTML en formato Base64. Nota: configurar este indicador puede aumentar significativamente el tamaño del archivo HTML de salida.

```csharp
public bool ExportEmbeddedFonts { get; set; }
```

## Ejemplos

Muestra cómo determinar dónde almacenar las fuentes incrustadas al exportar un documento a HTML.

```csharp
Document doc = new Document(MyDir + "Embedded font.docx");

// Cuando exportamos un documento con fuentes incrustadas a .html,
// Aspose.Words puede colocar las fuentes en dos ubicaciones posibles.
// Establecer el indicador "ExportEmbeddedFonts" en "verdadero" almacenará los datos sin procesar de las fuentes incrustadas dentro de la hoja de estilos CSS.
// en la propiedad "url" de la regla "@font-face". Esto puede generar un archivo de hoja de estilos CSS enorme.
// y reducir la cantidad de archivos externos que creará esta conversión HTML.
// Si se establece este indicador en "falso", se creará un archivo para cada fuente.
// La hoja de estilo CSS se vinculará a cada archivo de fuente utilizando la propiedad "url" de la regla "@font-face".
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
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
