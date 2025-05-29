---
title: MarkdownLoadOptions.ImportUnderlineFormatting
linktitle: ImportUnderlineFormatting
articleTitle: ImportUnderlineFormatting
second_title: Aspose.Words para .NET
description: Descubre la propiedad ImportUnderlineFormatting de MarkdownLoadOptions. Controla el formato del texto subrayado con una sencilla configuración booleana. ¡Mejora tu experiencia con Markdown!
type: docs
weight: 20
url: /es/net/aspose.words.loading/markdownloadoptions/importunderlineformatting/
---
## MarkdownLoadOptions.ImportUnderlineFormatting property

Obtiene o establece un valor booleano que indica si se debe reconocer una secuencia de dos caracteres más "++" como formato de texto subrayado. El valor predeterminado es`FALSO` .

```csharp
public bool ImportUnderlineFormatting { get; set; }
```

## Ejemplos

Muestra cómo reconocer los caracteres más "++" como formato de texto subrayado.

```csharp
using (MemoryStream stream = new MemoryStream(Encoding.ASCII.GetBytes("++12 and B++")))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = true };
    Document doc = new Document(stream, loadOptions);

    Paragraph para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.Single, para.Runs[0].Font.Underline);

    loadOptions = new MarkdownLoadOptions() { ImportUnderlineFormatting = false };
    doc = new Document(stream, loadOptions);

    para = (Paragraph)doc.GetChild(NodeType.Paragraph, 0, true);
    Assert.AreEqual(Underline.None, para.Runs[0].Font.Underline);
}
```

### Ver también

* class [MarkdownLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
