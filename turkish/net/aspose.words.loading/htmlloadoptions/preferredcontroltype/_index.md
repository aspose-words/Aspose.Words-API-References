---
title: HtmlLoadOptions.PreferredControlType
second_title: Aspose.Words for .NET API Referansı
description: HtmlLoadOptions mülk. İçe aktarılan input ve select öğelerini temsil edecek tercih edilen belge düğümü türünü alır veya ayarlar. Varsayılan değerFormField .
type: docs
weight: 50
url: /tr/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

İçe aktarılan &lt;input&gt; ve &lt;select&gt; öğelerini temsil edecek tercih edilen belge düğümü türünü alır veya ayarlar. Varsayılan değerFormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

### Notlar

Lütfen bu özelliğin ayarlanmasının, içe aktarılan tüm kontrollerin belirtilen tipte olacağını garanti etmediğini unutmayın. Bir HTML kontrolü, tercih edilen tipteki belge düğümleriyle temsil edilemezse, Aspose.Words, uyumlu bir kullanacaktır.[`HtmlControlType`](../../htmlcontroltype/) bu kontrol için.

### Örnekler

İçe aktarılan &lt;input&gt; ve &lt;select&gt; öğelerini temsil edecek tercih edilen belge düğümü türünün nasıl ayarlanacağını gösterir.

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
* ad alanı [Aspose.Words.Loading](../../htmlloadoptions/)
* toplantı [Aspose.Words](../../../)


