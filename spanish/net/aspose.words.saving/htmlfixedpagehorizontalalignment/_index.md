---
title: HtmlFixedPageHorizontalAlignment Enum
linktitle: HtmlFixedPageHorizontalAlignment
articleTitle: HtmlFixedPageHorizontalAlignment
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.HtmlFixedPageHorizontalAlignment para un control preciso de la alineación de páginas en sus documentos HTML. ¡Mejore el formato de sus documentos hoy mismo!
type: docs
weight: 5820
url: /es/net/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enumeration

Especifica la alineación horizontal de las páginas en el documento HTML de salida.

```csharp
public enum HtmlFixedPageHorizontalAlignment
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| Left | `0` | Alinear páginas a la izquierda. |
| Center | `1` | Centrar páginas. Este es el valor predeterminado. |
| Right | `2` | Alinear páginas a la derecha. |

## Ejemplos

Muestra cómo establecer la alineación horizontal de las páginas al guardar un documento en HTML.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    PageHorizontalAlignment = pageHorizontalAlignment
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css");

switch (pageHorizontalAlignment)
{
    case HtmlFixedPageHorizontalAlignment.Center:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Left:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Right:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }").Success);
        break;
}
```

### Ver también

* espacio de nombres [Aspose.Words.Saving](../../aspose.words.saving/)
* asamblea [Aspose.Words](../../)
