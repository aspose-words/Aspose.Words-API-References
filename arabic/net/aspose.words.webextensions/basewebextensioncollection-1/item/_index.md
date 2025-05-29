---
title: BaseWebExtensionCollection1.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية BaseWebExtensionCollection لإدارة العناصر بسهولة حسب الفهرس. بسّط تطويرك مع معالجة بيانات فعّالة اليوم!
type: docs
weight: 20
url: /ar/net/aspose.words.webextensions/basewebextensioncollection-1/item/
---
## BaseWebExtensionCollection&lt;T&gt; indexer

يحصل على عنصر أو يعينه في الفهرس المحدد.

```csharp
public T this[int index] { get; set; }
```

| معامل | وصف |
| --- | --- |
| index | مؤشر يعتمد على الصفر للعنصر. |

## أمثلة

يوضح كيفية العمل مع مجموعة ملحقات الويب الخاصة بالمستند.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// طباعة كافة خصائص ملحق الويب الخاص بالمستند.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// إزالة ملحق الويب.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### أنظر أيضا

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* مساحة الاسم [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* المجسم [Aspose.Words](../../../)
