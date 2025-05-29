---
title: HtmlLoadOptions.ConvertSvgToEmf
linktitle: ConvertSvgToEmf
articleTitle: ConvertSvgToEmf
second_title: Aspose.Words para .NET
description: Descubra la propiedad ConvertSvgToEmf de HtmlLoadOptions. Controle fácilmente la conversión de SVG a EMF para una calidad de imagen óptima. El valor predeterminado es falso; ¡mantenga los SVG intactos!
type: docs
weight: 30
url: /es/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

Obtiene o establece un valor que indica si se deben convertir las imágenes SVG cargadas al formato EMF. El valor predeterminado es`FALSO` y, si es posible, las imágenes SVG cargadas se almacenan tal cual sin conversión.

```csharp
public bool ConvertSvgToEmf { get; set; }
```

## Observaciones

Las versiones más recientes de MS Word admiten imágenes SVG de forma nativa. Si la versión de MS Word especificada en las opciones de carga admite SVG, Aspose.Words almacenará las imágenes SVG tal cual, sin convertirlas. Si no admite SVG, las imágenes SVG cargadas se convertirán al formato EMF.

Sin embargo, si esta opción está configurada en`verdadero` Aspose.Words convertirá las imágenes SVG cargadas a EMF incluso si las imágenes SVG son compatibles con la versión especificada de MS Word.

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

* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
