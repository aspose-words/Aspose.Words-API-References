---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlFixedSaveOptions propiedad. Especifica si los recursos SVG deben incrustarse en el documento HTML. El valor predeterminado esverdadero .
type: docs
weight: 70
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

Especifica si los recursos SVG deben incrustarse en el documento HTML. El valor predeterminado es`verdadero` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

### Ejemplos

Muestra cómo determinar dónde almacenar objetos SVG al exportar un documento a HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Cuando exportamos un documento con objetos SVG a .html,
// Aspose.Words puede colocar estos objetos en dos ubicaciones posibles.
// Establecer el indicador "ExportEmbeddedSvg" en "true" incrustará todos los datos sin procesar del objeto SVG
// dentro del HTML de salida, dentro de <image> etiquetas.
// Establecer este indicador en "falso" creará un archivo en el sistema de archivos local para cada objeto SVG.
// El HTML se vinculará a cada archivo utilizando el atributo "datos" de un objeto <objeto> etiqueta.
HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    ExportEmbeddedSvg = exportSvgs
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs.html");

if (exportSvgs)
{
    Assert.False(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<image id=\"image004\" xlink:href=.+/>").Success);
}
else
{
    Assert.True(File.Exists(ArtifactsDir + "HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001.svg"));
    Assert.True(Regex.Match(outDocContents,
        "<object type=\"image/svg[+]xml\" data=\"HtmlFixedSaveOptions.ExportEmbeddedSvgs/svg001[.]svg\"></object>").Success);
}
```

### Ver también

* class [HtmlFixedSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* asamblea [Aspose.Words](../../../)


