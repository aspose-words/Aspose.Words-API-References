---
title: HtmlControlType Enum
linktitle: HtmlControlType
articleTitle: HtmlControlType
second_title: .NET için Aspose.Words
description: HTML girdilerinin ve seçili öğelerin sorunsuz bir şekilde içe aktarılması için Aspose.Words.HtmlControlType enum'unu keşfedin ve belge işleme yeteneklerinizi geliştirin.
type: docs
weight: 4060
url: /tr/net/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enumeration

HTML'den içe aktarılan &lt;input&gt; ve &lt;select&gt; öğelerini temsil eden belge düğümlerinin türü.

```csharp
public enum HtmlControlType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| FormField | `0` | Bir form alanı. |
| StructuredDocumentTag | `1` | Yapılandırılmış bir belge etiketi |

## Örnekler

İçeri aktarılan &lt;input&gt; ve &lt;select&gt; öğelerini temsil edecek tercih edilen belge düğümü türünün nasıl ayarlanacağını gösterir.

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

### Ayrıca bakınız

* ad alanı [Aspose.Words.Loading](../../aspose.words.loading/)
* toplantı [Aspose.Words](../../)
