---
title: HtmlControlType Enum
linktitle: HtmlControlType
articleTitle: HtmlControlType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.HtmlControlType enum لاستيراد إدخال HTML وعناصر التحديد بسلاسة، مما يعزز قدرات معالجة المستندات لديك.
type: docs
weight: 4060
url: /ar/net/aspose.words.loading/htmlcontroltype/
---
## HtmlControlType enumeration

نوع عقد المستندات التي تمثل عناصر &lt;input&gt; و&lt;select&gt; المستوردة من HTML.

```csharp
public enum HtmlControlType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| FormField | `0` | حقل النموذج. |
| StructuredDocumentTag | `1` | علامة مستند منظمة |

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

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)
