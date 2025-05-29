---
title: HtmlFixedSaveOptions.ExportEmbeddedCss
linktitle: ExportEmbeddedCss
articleTitle: ExportEmbeddedCss
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad ExportEmbeddedCss de HtmlFixedSaveOptions mejora sus documentos HTML al incorporar CSS para un estilo impecable. ¡Optimice sus páginas web hoy mismo!
type: docs
weight: 40
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedcss/
---
## HtmlFixedSaveOptions.ExportEmbeddedCss property

Especifica si la CSS (hoja de estilo en cascada) debe incrustarse en el documento HTML.

```csharp
public bool ExportEmbeddedCss { get; set; }
```

## Ejemplos

Muestra cómo determinar dónde almacenar las hojas de estilo CSS al exportar un documento a HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Cuando exportamos un documento a html, Aspose.Words también creará una hoja de estilos CSS para formatear el documento.
// Al establecer el indicador "ExportEmbeddedCss" en "verdadero", se guarda la hoja de estilo CSS en un archivo .css.
// y vincular al archivo desde el documento html usando un elemento <link>.
// Establecer el indicador en "falso" incrustará la hoja de estilo CSS dentro del documento HTML,
// que creará solo un archivo en lugar de dos.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedCss = exportEmbeddedCss
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss.html");

if (exportEmbeddedCss)
{
    Assert.True(Regex.Match(outDocContents, "<style type=\"text/css\">").Success);
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
else
{
    Assert.True(Regex.Match(outDocContents,
        "<link rel=\"stylesheet\" type=\"text/css\" href=\"HtmlFixedSaveOptions[.]ExportEmbeddedCss/styles[.]css\" media=\"all\" />").Success);
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedCss/styles.css"));
}
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
