---
title: BaseWebExtensionCollection1.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة BaseWebExtensionCollection GetEnumerator للتنقل بسهولة عبر المجموعات، مما يعزز كفاءة التطوير وإدارة الكود.
type: docs
weight: 50
url: /ar/net/aspose.words.webextensions/basewebextensioncollection-1/getenumerator/
---
## BaseWebExtensionCollection&lt;T&gt;.GetEnumerator method

يعيد مُعَدِّدًا يمكنه التكرار خلال مجموعة.

```csharp
public IEnumerator<T> GetEnumerator()
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
