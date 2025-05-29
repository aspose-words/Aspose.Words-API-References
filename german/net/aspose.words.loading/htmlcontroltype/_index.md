---
title: HtmlControlType Enum
linktitle: HtmlControlType
articleTitle: HtmlControlType
second_title: Aspose.Words für .NET
description: Entdecken Sie die Aufzählung Aspose.Words.HtmlControlType für den nahtlosen Import von HTML-Eingabe- und Auswahlelementen und verbessern Sie so Ihre Dokumentverarbeitungsfunktionen.
type: docs
weight: 4060
url: /de/net/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enumeration

Art der Dokumentknoten, die aus HTML importierte &lt;input&gt;- und &lt;select&gt;-Elemente darstellen.

```csharp
public enum HtmlControlType
```

### Werte

| Name | Wert | Beschreibung |
| --- | --- | --- |
| FormField | `0` | Ein Formularfeld. |
| StructuredDocumentTag | `1` | Ein strukturiertes Dokument-Tag |

## Beispiele

Zeigt, wie der bevorzugte Typ von Dokumentknoten festgelegt wird, die importierte &lt;input&gt;- und &lt;select&gt;-Elemente darstellen.

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

* namensraum [Aspose.Words.Loading](../../aspose.words.loading/)
* Montage [Aspose.Words](../../)
