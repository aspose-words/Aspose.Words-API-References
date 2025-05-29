---
title: HtmlLoadOptions.PreferredControlType
linktitle: PreferredControlType
articleTitle: PreferredControlType
second_title: Aspose.Words för .NET
description: Upptäck HtmlLoadOptions egenskap PreferredControlType för att anpassa dokumentnodtyper för importerade indata och välja element. Optimera dina formulär utan ansträngning!
type: docs
weight: 50
url: /sv/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

Hämtar eller ställer in önskad typ av dokumentnoder som representerar importerade &lt;input&gt;- och &lt;select&gt;-element. Standardvärdet ärFormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

## Anmärkningar

Observera att inställningen av den här egenskapen inte garanterar att alla importerade kontroller kommer att vara av den angivna typen. Om en HTML-kontroll inte kan representeras med dokumentnoder av den föredragna typen kommer Aspose.Words att använda en kompatibel[`HtmlControlType`](../../htmlcontroltype/) för den kontrollen.

## Exempel

Visar hur man anger önskad typ av dokumentnoder som representerar importerade &lt;input&gt;- och &lt;select&gt;-element.

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

### Se även

* enum [HtmlControlType](../../htmlcontroltype/)
* class [HtmlLoadOptions](../)
* namnutrymme [Aspose.Words.Loading](../../../aspose.words.loading/)
* hopsättning [Aspose.Words](../../../)
