---
title: HtmlLoadOptions.PreferredControlType
second_title: Aspose.Words per .NET API Reference
description: HtmlLoadOptions proprietà. Ottiene o imposta il tipo preferito di nodi di documento che rappresenteranno gli elementi input e select importati. Il valore predefinito èFormField .
type: docs
weight: 50
url: /it/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

Ottiene o imposta il tipo preferito di nodi di documento che rappresenteranno gli elementi &lt;input&gt; e &lt;select&gt; importati. Il valore predefinito èFormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

### Osservazioni

Tieni presente che l'impostazione di questa proprietà non garantisce che tutti i controlli importati saranno del tipo specificato. Se un controllo HTML non è rappresentabile con nodi di documento del tipo preferito, Aspose.Words utilizzerà un controllo compatibile[`HtmlControlType`](../../htmlcontroltype/) per quel controllo.

### Esempi

Mostra come impostare il tipo preferito di nodi di documento che rappresenteranno gli elementi &lt;input&gt; e &lt;select&gt; importati.

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

### Guarda anche

* enum [HtmlControlType](../../htmlcontroltype/)
* class [HtmlLoadOptions](../)
* spazio dei nomi [Aspose.Words.Loading](../../htmlloadoptions/)
* assemblea [Aspose.Words](../../../)


