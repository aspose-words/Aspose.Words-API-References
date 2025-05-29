---
title: HtmlSaveOptions.ExportRelativeFontSize
linktitle: ExportRelativeFontSize
articleTitle: ExportRelativeFontSize
second_title: Aspose.Words para .NET
description: Descubra la propiedad HtmlSaveOptions ExportRelativeFontSize para personalizar el tamaño de fuente en formatos HTML, MHTML o EPUB. ¡Mejore la legibilidad fácilmente!
type: docs
weight: 230
url: /es/net/aspose.words.saving/htmlsaveoptions/exportrelativefontsize/
---
## HtmlSaveOptions.ExportRelativeFontSize property

Especifica si los tamaños de fuente deben imprimirse en unidades relativas al guardar en HTML, MHTML o EPUB. El valor predeterminado es`FALSO` .

```csharp
public bool ExportRelativeFontSize { get; set; }
```

## Observaciones

En muchos documentos existentes (HTML, IDPF, EPUB), el tamaño de las fuentes se especifica en unidades relativas. Esto permite que las aplicaciones ajusten el tamaño del texto al visualizar o procesar documentos. Por ejemplo, Microsoft Internet Explorer tiene el submenú "Ver-&gt;Tamaño del texto", mientras que Adobe Digital Editions tiene dos botones: Aumentar/Disminuir el tamaño del texto. Si espera que esta función funcione, configure`ExportRelativeFontSize` propiedad a`verdadero` .

El modelo de documento de Aspose Words contiene y opera únicamente con unidades de tamaño de fuente absolutas. Las unidades relativas requieren una lógica adicional para recalcularse a partir de un tamaño inicial (estándar). Tamaño de fuente de**Normal** El estilo de documento se toma como estándar. Por ejemplo, si**Normal** tiene una fuente de 12 puntos y parte del texto es de 18 puntos, entonces se emitirá como output **1,5em.** al HTML.

Cuando esta opción está habilitada, los elementos del documento, excepto el texto, seguirán teniendo tamaños absolutos. Además, algunos atributos relacionados con el texto podrían expresarse de forma absoluta. En particular, el interlineado especificado con la regla "exactly" podría producir resultados no deseados al escalar el texto. Por lo tanto, los documentos fuente deben diseñarse y probarse correctamente al exportar con...`ExportRelativeFontSize` empezar a`verdadero`.

## Ejemplos

Muestra cómo utilizar tamaños de fuente relativos al guardar en .html.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Default font size, ");
builder.Font.Size = 24;
builder.Writeln("2x default font size,");
builder.Font.Size = 96;
builder.Write("8x default font size");

// Cuando guardamos el documento en HTML, podemos pasar un objeto SaveOptions
// para determinar si se utilizarán tamaños de fuente relativos o absolutos.
// Establezca el indicador "ExportRelativeFontSize" en "verdadero" para declarar tamaños de fuente
 // utilizando la unidad de medida "em", que es un factor que multiplica el tamaño de fuente actual.
// Establezca el indicador "ExportRelativeFontSize" en "falso" para declarar tamaños de fuente
// utilizando la unidad de medida "pt", que es el tamaño absoluto de la fuente en puntos.
HtmlSaveOptions options = new HtmlSaveOptions { ExportRelativeFontSize = exportRelativeFontSize };

doc.Save(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.RelativeFontSize.html");

if (exportRelativeFontSize)
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:2em\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:8em\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<body style=\"font-family:'Times New Roman'; font-size:12pt\">" +
            "<div>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                    "<span>Default font size, </span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:24pt\">" +
                    "<span>2x default font size,</span>" +
                "</p>" +
                "<p style=\"margin-top:0pt; margin-bottom:0pt; font-size:96pt\">" +
                    "<span>8x default font size</span>" +
                "</p>" +
            "</div>" +
        "</body>"));
}
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
