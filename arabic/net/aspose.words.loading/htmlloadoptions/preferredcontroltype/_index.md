---
title: HtmlLoadOptions.PreferredControlType
linktitle: PreferredControlType
articleTitle: PreferredControlType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PreferredControlType في HtmlLoadOptions لتخصيص أنواع عقد المستندات للمدخلات المستوردة وعناصر التحديد. حسّن نماذجك بسهولة!
type: docs
weight: 50
url: /ar/net/aspose.words.loading/htmlloadoptions/preferredcontroltype/
---
## HtmlLoadOptions.PreferredControlType property

يحصل على أو يعين النوع المفضل من عقد المستندات التي ستمثل عناصر &lt;input&gt; و&lt;select&gt; المستوردة. القيمة الافتراضية هيFormField .

```csharp
public HtmlControlType PreferredControlType { get; set; }
```

## ملاحظات

يرجى ملاحظة أن تعيين هذه الخاصية لا يضمن أن تكون جميع عناصر التحكم المستوردة من النوع المحدد. إذا لم يكن من الممكن تمثيل عنصر تحكم HTML باستخدام عقد المستندات من النوع المفضل، فسوف يستخدم Aspose.Words عنصر تحكم متوافق[`HtmlControlType`](../../htmlcontroltype/) لهذا التحكم.

## أمثلة

يوضح كيفية تعيين النوع المفضل لعقد المستندات التي ستمثل عناصر &lt;input&gt; و&lt;select&gt; المستوردة.

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
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
