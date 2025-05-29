---
title: HtmlMetafileFormat Enum
linktitle: HtmlMetafileFormat
articleTitle: HtmlMetafileFormat
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.Saving.HtmlMetafileFormat para guardar metarchivos sin problemas en documentos HTML. ¡Mejore su experiencia de conversión de documentos hoy mismo!
type: docs
weight: 5840
url: /es/net/aspose.words.saving/htmlmetafileformat/
---
## HtmlMetafileFormat enumeration

Indica el formato en el que se guardan los metarchivos en los documentos HTML.

```csharp
public enum HtmlMetafileFormat
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Png | `0` | Los metarchivos se procesan en imágenes PNG rasterizadas. |
| Svg | `1` | Los metarchivos se convierten en imágenes SVG vectoriales. |
| EmfOrWmf | `2` | Los metarchivos se guardan tal cual, sin conversión. |

## Ejemplos

Muestra cómo convertir objetos SVG a un formato diferente al guardar documentos HTML.

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' ancho='500' alto='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// Utilice 'ConvertSvgToEmf' para revertir el comportamiento heredado
// donde todas las imágenes SVG cargadas desde un documento HTML se convirtieron a EMF.
// Ahora las imágenes SVG se cargan sin conversión
// si la versión de MS Word especificada en las opciones de carga admite imágenes SVG de forma nativa.
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

//Este documento contiene un elemento <svg> en forma de texto.
// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions
// para determinar cómo la operación de guardado maneja este objeto.
// Establezca la propiedad "MetafileFormat" en "HtmlMetafileFormat.Png" para convertirla en una imagen PNG.
// Al establecer la propiedad "MetafileFormat" en "HtmlMetafileFormat.Svg", se conserva como un objeto SVG.
// Establezca la propiedad "MetafileFormat" en "HtmlMetafileFormat.EmfOrWmf" para convertirla en un metarchivo.
HtmlSaveOptions options = new HtmlSaveOptions { MetafileFormat = htmlMetafileFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case HtmlMetafileFormat.Png:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
    case HtmlMetafileFormat.Svg:
        Assert.True(outDocContents.Contains(
            "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" versión=\"1.1\" ancho=\"499\" alto=\"40\">"));
        break;
    case HtmlMetafileFormat.EmfOrWmf:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
}
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
