---
title: MarkdownLoadOptions.PreserveEmptyLines
linktitle: PreserveEmptyLines
articleTitle: PreserveEmptyLines
second_title: Aspose.Words para .NET
description: Descubra cómo la propiedad PreserveEmptyLines de MarkdownLoadOptions mejora la carga de sus documentos Markdown al preservar las líneas vacías para una mejor legibilidad.
type: docs
weight: 30
url: /es/net/aspose.words.loading/markdownloadoptions/preserveemptylines/
---
## MarkdownLoadOptions.PreserveEmptyLines property

Obtiene o establece un valor booleano que indica si se deben conservar las líneas vacías mientras se carga unMarkdown document. El valor predeterminado es`FALSO` .

Normalmente, en Markdown, se ignoran las líneas vacías entre elementos a nivel de bloque. Las líneas vacías al principio y al final del documento también se ignoran. Esta opción permite importar dichas líneas vacías.

```csharp
public bool PreserveEmptyLines { get; set; }
```

## Ejemplos

Muestra cómo conservar una línea vacía mientras se carga un documento.

```csharp
string mdText = $"{Environment.NewLine}Line1{Environment.NewLine}{Environment.NewLine}Line2{Environment.NewLine}{Environment.NewLine}";
using (MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(mdText)))
{
    MarkdownLoadOptions loadOptions = new MarkdownLoadOptions() { PreserveEmptyLines = true };
    Document doc = new Document(stream, loadOptions);

    Assert.AreEqual("\rLine1\r\rLine2\r\f", doc.GetText());
}
```

### Ver también

* class [MarkdownLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
