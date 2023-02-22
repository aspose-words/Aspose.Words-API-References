---
title: HtmlLoadOptions.PreferredControlType
second_title: Referencia de API de Aspose.Words para .NET
description: HtmlLoadOptions propiedad. Obtiene o establece el tipo preferido de nodos de documento que representarán los elementos input y select importados. El valor predeterminado esFormField .
type: docs
weight: 50
url: /es/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

Obtiene o establece el tipo preferido de nodos de documento que representarán los elementos &lt;input&gt; y &lt;select&gt; importados. El valor predeterminado esFormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

### Observaciones

Tenga en cuenta que establecer esta propiedad no garantiza que todos los controles importados sean del tipo especificado. Si un control HTML no se puede representar con nodos de documentos del tipo preferido, Aspose.Words usará un control compatible[`HtmlControlType`](../../htmlcontroltype/) para ese control.

### Ejemplos

Muestra cómo establecer el tipo preferido de nodos de documentos que representarán los elementos &lt;input&gt; y &lt;select&gt; importados.

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

* enum [HtmlControlType](../../htmlcontroltype/)
* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../htmlloadoptions/)
* asamblea [Aspose.Words](../../../)


