---
title: BaseWebExtensionCollection1.Remove
linktitle: Remove
articleTitle: Remove
second_title: Aspose.Words لـ .NET
description: BaseWebExtensionCollection Remove طريقة. إزالة العنصر الموجود في الفهرس المحدد من المجموعة في C#.
type: docs
weight: 60
url: /ar/net/aspose.words.webextensions/basewebextensioncollection-1/remove/
---
## BaseWebExtensionCollection&lt;T&gt;.Remove method

إزالة العنصر الموجود في الفهرس المحدد من المجموعة.

```csharp
public void Remove(int index)
```

| معامل | يكتب | وصف |
| --- | --- | --- |
| index | Int32 | الفهرس الصفري لعنصر المجموعة. |

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
