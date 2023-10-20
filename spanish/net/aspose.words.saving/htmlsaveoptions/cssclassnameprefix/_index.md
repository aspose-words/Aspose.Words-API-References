---
title: HtmlSaveOptions.CssClassNamePrefix
linktitle: CssClassNamePrefix
articleTitle: CssClassNamePrefix
second_title: Aspose.Words para .NET
description: HtmlSaveOptions CssClassNamePrefix propiedad. Especifica un prefijo que se agrega a todos los nombres de clases CSS. El valor predeterminado es una cadena vacía y los nombres de clases CSS generados no tienen un prefijo común en C#.
type: docs
weight: 30
url: /es/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

Especifica un prefijo que se agrega a todos los nombres de clases CSS. El valor predeterminado es una cadena vacía y los nombres de clases CSS generados no tienen un prefijo común.

```csharp
public string CssClassNamePrefix { get; set; }
```

### Excepciones

| excepción | condición |
| --- | --- |
| ArgumentException | El valor no está vacío y no es un identificador CSS válido. |

## Observaciones

Si este valor no está vacío, todas las clases CSS generadas por Aspose.Words comenzarán con el prefijo especificado. Esto puede ser útil, por ejemplo, si agrega CSS personalizado a los documentos generados y desea evitar conflictos de nombres class .

Si el valor no es`nulo` o vacío, debe ser un identificador CSS válido.

## Ejemplos

Muestra cómo guardar un documento en HTML y agregar un prefijo a todos sus nombres de clases CSS.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    CssClassNamePrefix = "myprefix-"
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html");

Assert.True(outDocContents.Contains("<p class=\"myprefix-Header\">"));
Assert.True(outDocContents.Contains("<p class=\"myprefix-Footer\">"));

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.css");

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n" +
                                    ".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n"));
```

### Ver también

* class [HtmlSaveOptions](../)
* espacio de nombres [Aspose.Words.Saving](../../../aspose.words.saving/)
* asamblea [Aspose.Words](../../../)
