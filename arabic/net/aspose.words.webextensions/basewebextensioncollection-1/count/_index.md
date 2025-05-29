---
title: BaseWebExtensionCollection1.Count
linktitle: Count
articleTitle: Count
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Count الخاصة بـ BaseWebExtensionCollection لاسترداد العدد الإجمالي للعناصر بسهولة، مما يعزز كفاءة تطوير الويب لديك.
type: docs
weight: 10
url: /ar/net/aspose.words.webextensions/basewebextensioncollection-1/count/
---
## BaseWebExtensionCollection&lt;T&gt;.Count property

يحصل على عدد العناصر الموجودة في المجموعة.

```csharp
public int Count { get; }
```

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
