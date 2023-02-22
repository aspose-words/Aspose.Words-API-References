---
title: HtmlLoadOptions.PreferredControlType
second_title: Aspose.Words لمراجع .NET API
description: HtmlLoadOptions ملكية. الحصول على أو تعيين النوع المفضل لعقد المستندات التي ستمثل العناصر المستوردة input و select . القيمة الافتراضية هيFormField .
type: docs
weight: 50
url: /ar/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

الحصول على أو تعيين النوع المفضل لعقد المستندات التي ستمثل العناصر المستوردة &lt;input&gt; و &lt;select&gt; . القيمة الافتراضية هيFormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

### ملاحظات

يُرجى ملاحظة أن إعداد هذه الخاصية لا يضمن أن جميع عناصر التحكم المستوردة ستكون من النوع المحدد.[`HtmlControlType`](../../htmlcontroltype/) من أجل هذا التحكم.

### أمثلة

يوضح كيفية تعيين النوع المفضل لعقد المستند التي ستمثل العناصر المستوردة &lt;input&gt; و &lt;select&gt;.

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

### أنظر أيضا

* enum [HtmlControlType](../../htmlcontroltype/)
* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../htmlloadoptions/)
* المجسم [Aspose.Words](../../../)


