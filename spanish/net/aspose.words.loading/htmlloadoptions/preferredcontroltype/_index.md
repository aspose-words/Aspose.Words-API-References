---
title: HtmlLoadOptions.PreferredControlType
linktitle: PreferredControlType
articleTitle: PreferredControlType
second_title: Aspose.Words para .NET
description: Descubra la propiedad PreferredControlType de HtmlLoadOptions para personalizar los tipos de nodos de documento para las entradas importadas y los elementos de selección. ¡Optimice sus formularios fácilmente!
type: docs
weight: 50
url: /es/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

Obtiene o establece el tipo preferido de nodos de documento que representarán los elementos &lt;input&gt; y &lt;select&gt; importados. El valor predeterminado esFormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

## Observaciones

Tenga en cuenta que configurar esta propiedad no garantiza que todos los controles importados sean del tipo especificado. Si un control HTML no se puede representar con nodos de documento del tipo preferido, Aspose.Words utilizará un control compatible.[`HtmlControlType`](../../htmlcontroltype/) para ese control.

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

* enum [HtmlControlType](../../htmlcontroltype/)
* class [HtmlLoadOptions](../)
* espacio de nombres [Aspose.Words.Loading](../../../aspose.words.loading/)
* asamblea [Aspose.Words](../../../)
