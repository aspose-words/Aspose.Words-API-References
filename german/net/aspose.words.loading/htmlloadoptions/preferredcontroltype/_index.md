---
title: HtmlLoadOptions.PreferredControlType
second_title: Aspose.Words für .NET-API-Referenz
description: HtmlLoadOptions eigendom. Ruft den bevorzugten Typ von Dokumentknoten ab oder legt ihn fest der importierte input und selectElemente darstellt. Der Standardwert istFormField .
type: docs
weight: 50
url: /de/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

Ruft den bevorzugten Typ von Dokumentknoten ab oder legt ihn fest, der importierte &lt;input&gt;- und &lt;select&gt;-Elemente darstellt. Der Standardwert istFormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

### Bemerkungen

Bitte beachten Sie, dass das Setzen dieser Eigenschaft nicht garantiert, dass alle importierten Steuerelemente vom angegebenen Typ sind. Wenn ein HTML-Steuerelement nicht mit Dokumentknoten des bevorzugten Typs darstellbar ist, verwendet Aspose.Words ein kompatibles[`HtmlControlType`](../../htmlcontroltype/) für diese Kontrolle.

### Beispiele

Zeigt, wie Sie den bevorzugten Typ von Dokumentknoten festlegen, die importierte &lt;input&gt;- und &lt;select&gt;-Elemente darstellen.

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

### Siehe auch

* enum [HtmlControlType](../../htmlcontroltype/)
* class [HtmlLoadOptions](../)
* namensraum [Aspose.Words.Loading](../../htmlloadoptions/)
* Montage [Aspose.Words](../../../)


