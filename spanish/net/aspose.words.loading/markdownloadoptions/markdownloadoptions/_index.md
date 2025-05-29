---
title: MarkdownLoadOptions
linktitle: MarkdownLoadOptions
articleTitle: MarkdownLoadOptions
second_title: Aspose.Words para .NET
description: Descubra el constructor MarkdownLoadOptions para inicializar fácilmente instancias de MarkdownLoadOptions para un mejor procesamiento y personalización de documentos.
type: docs
weight: 10
url: /es/net/aspose.words.loading/markdownloadoptions/markdownloadoptions/
---
## MarkdownLoadOptions constructor

Inicializa una nueva instancia de[`MarkdownLoadOptions`](../) clase.

```csharp
public MarkdownLoadOptions()
```

## Observaciones

Se establece automáticamente[`LoadFormat`](../../../aspose.words/loadformat/) aMarkdown .

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
