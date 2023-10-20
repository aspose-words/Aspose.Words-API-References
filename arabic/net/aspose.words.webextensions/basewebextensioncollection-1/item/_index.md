---
title: BaseWebExtensionCollection1.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: BaseWebExtensionCollection Item ملكية. الحصول على عنصر أو تعيينه في الفهرس المحدد في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.webextensions/basewebextensioncollection-1/item/
---
## BaseWebExtensionCollection&lt;T&gt; indexer

الحصول على عنصر أو تعيينه في الفهرس المحدد.

```csharp
public T this[int index] { get; set; }
```

| معامل | وصف |
| --- | --- |
| index | الفهرس الصفري للعنصر. |

## أمثلة

يوضح كيفية العمل مع مجموعة ملحقات الويب الخاصة بالمستند.

```csharp
Document doc = new Document(MyDir + "Web extension.docx");

Assert.AreEqual(1, doc.WebExtensionTaskPanes.Count);

// اطبع كافة خصائص ملحق الويب الخاص بالمستند.
WebExtensionPropertyCollection webExtensionPropertyCollection = doc.WebExtensionTaskPanes[0].WebExtension.Properties;
using (IEnumerator<WebExtensionProperty> enumerator = webExtensionPropertyCollection.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        WebExtensionProperty webExtensionProperty = enumerator.Current;
        Console.WriteLine($"Binding name: {webExtensionProperty.Name}; Binding value: {webExtensionProperty.Value}");
    }
}

// قم بإزالة ملحق الويب.
doc.WebExtensionTaskPanes.Remove(0);

Assert.AreEqual(0, doc.WebExtensionTaskPanes.Count);
```

### أنظر أيضا

* class [BaseWebExtensionCollection&lt;T&gt;](../)
* مساحة الاسم [Aspose.Words.WebExtensions](../../../aspose.words.webextensions/)
* المجسم [Aspose.Words](../../../)
