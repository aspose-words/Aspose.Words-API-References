---
title: HtmlControlType Enum
linktitle: HtmlControlType
articleTitle: HtmlControlType
second_title: Aspose.Words per .NET
description: Scopri l'enum Aspose.Words.HtmlControlType per un'importazione fluida di input HTML e seleziona elementi, migliorando le capacità di elaborazione dei documenti.
type: docs
weight: 4060
url: /it/net/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enumeration

Tipo di nodi del documento che rappresentano gli elementi &lt;input&gt; e &lt;select&gt; importati da HTML.

```csharp
public enum HtmlControlType
```

### I valori

| Nome | Valore | Descrizione |
| --- | --- | --- |
| FormField | `0` | Un campo modulo. |
| StructuredDocumentTag | `1` | Un tag di documento strutturato |

## Esempi

Mostra come impostare il tipo preferito di nodi del documento che rappresenteranno gli elementi &lt;input&gt; e &lt;select&gt; importati.

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

* spazio dei nomi [Aspose.Words.Loading](../../aspose.words.loading/)
* assemblea [Aspose.Words](../../)
