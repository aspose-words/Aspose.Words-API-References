---
title: HtmlLoadOptions.PreferredControlType
linktitle: PreferredControlType
articleTitle: PreferredControlType
second_title: .NET için Aspose.Words
description: İçeri aktarılan girdiler ve seçili öğeler için belge düğüm türlerini özelleştirmek üzere HtmlLoadOptions' PreferredControlType özelliğini keşfedin. Formlarınızı zahmetsizce optimize edin!
type: docs
weight: 50
url: /tr/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

İçeri aktarılan &lt;input&gt; ve &lt;select&gt; öğelerini temsil edecek tercih edilen belge düğümü türünü alır veya ayarlar. Varsayılan değerFormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

## Notlar

Lütfen bu özelliği ayarlamanın, içe aktarılan tüm denetimlerin belirtilen türde olacağını garanti etmediğini unutmayın. Bir HTML denetimi tercih edilen türdeki belge düğümleriyle temsil edilemiyorsa, Aspose.Words uyumlu bir kullanacaktır.[`HtmlControlType`](../../htmlcontroltype/) bu kontrol için.

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

* enum [HtmlControlType](../../htmlcontroltype/)
* class [HtmlLoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
