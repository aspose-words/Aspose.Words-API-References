---
title: HtmlControlType Enum
linktitle: HtmlControlType
articleTitle: HtmlControlType
second_title: Aspose.Words para .NET
description: Descubra la enumeración Aspose.Words.HtmlControlType para una importación perfecta de elementos de entrada y selección HTML, mejorando sus capacidades de procesamiento de documentos.
type: docs
weight: 4060
url: /es/net/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enumeration

Tipo de nodos de documento que representan elementos &lt;input&gt; y &lt;select&gt; importados desde HTML.

```csharp
public enum HtmlControlType
```

### Valores

| Nombre | Valor | Descripción |
| --- | --- | --- |
| FormField | `0` | Un campo de formulario. |
| StructuredDocumentTag | `1` | Una etiqueta de documento estructurada |

## Ejemplos

Muestra cómo establecer el tipo preferido de nodos de documento que representarán los elementos &lt;input&gt; y &lt;select&gt; importados.

```csharp
const string html = @"
    <html>
        <select name='ComboBox' size='1'>
            <option value='val1'>item1</option>
            <option value='val2'></option>
        </select>
    </html>
";

HtmlLoadOptions htmlLoadOptions = new HtmlLoadOptions();
htmlLoadOptions.PreferredControlType = HtmlControlType.StructuredDocumentTag;

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), htmlLoadOptions);
NodeCollection nodes = doc.GetChildNodes(NodeType.StructuredDocumentTag, true);

StructuredDocumentTag tag = (StructuredDocumentTag) nodes[0];
```

### Ver también

* espacio de nombres [Aspose.Words.Loading](../../aspose.words.loading/)
* asamblea [Aspose.Words](../../)
