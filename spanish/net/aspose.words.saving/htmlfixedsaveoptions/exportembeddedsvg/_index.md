---
title: HtmlFixedSaveOptions.ExportEmbeddedSvg
linktitle: ExportEmbeddedSvg
articleTitle: ExportEmbeddedSvg
second_title: Aspose.Words para .NET
description: Descubra la propiedad ExportEmbeddedSvg de HtmlFixedSaveOptions: incruste fácilmente recursos SVG en sus documentos HTML para mejorar la visualización. Valor predeterminado verdadero.
type: docs
weight: 70
url: /es/net/aspose.words.saving/htmlfixedsaveoptions/exportembeddedsvg/
---
## HtmlFixedSaveOptions.ExportEmbeddedSvg property

Especifica si los recursos SVG deben incrustarse en el documento HTML. El valor predeterminado es`verdadero` .

```csharp
public bool ExportEmbeddedSvg { get; set; }
```

## Ejemplos

Muestra cómo determinar dónde almacenar los objetos SVG al exportar un documento a HTML.

```csharp
Document doc = new Document(MyDir + "Images.docx");

// Cuando exportamos un documento con objetos SVG a .html,
// Aspose.Words puede colocar estos objetos en dos ubicaciones posibles.
// Si se establece el indicador "ExportEmbeddedSvg" en "verdadero", se integrarán todos los datos sin procesar del objeto SVG
// dentro del HTML de salida, dentro de las etiquetas <image>.
// Establecer esta bandera como "falso" creará un archivo en el sistema de archivos local para cada objeto SVG.
// El HTML se vinculará a cada archivo utilizando el atributo "data" de una etiqueta <object>.
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
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
