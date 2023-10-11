---
title: HtmlLoadOptions.PreferredControlType
second_title: Aspose.Words لمراجع .NET API
description: HtmlLoadOptions ملكية. الحصول على أو تعيين النوع المفضل لعقد المستند التي ستمثل عناصر input وselect المستوردة. القيمة الافتراضية هيFormField .
type: docs
weight: 50
url: /ar/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

الحصول على أو تعيين النوع المفضل لعقد المستند التي ستمثل عناصر &lt;input&gt; و&lt;select&gt; المستوردة. القيمة الافتراضية هيFormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

### ملاحظات

يرجى ملاحظة أن تعيين هذه الخاصية لا يضمن أن جميع عناصر التحكم المستوردة ستكون من النوع المحدد. إذا كان عنصر تحكم HTML غير قابل للتمثيل مع عقد المستند من النوع المفضل، فسوف يستخدم Aspose.Words عنصرًا متوافقًا[`HtmlControlType`](../../htmlcontroltype/) لهذا التحكم.

### أمثلة

يوضح كيفية تعيين النوع المفضل لعقد المستند التي ستمثل عناصر &lt;input&gt; و&lt;select&gt; المستوردة.

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


