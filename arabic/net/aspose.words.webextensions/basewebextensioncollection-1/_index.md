---
title: BaseWebExtensionCollectionT Class
linktitle: BaseWebExtensionCollectionT
articleTitle: BaseWebExtensionCollectionT
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.WebExtensions.BaseWebExtensionCollection1T، وهي أداة أساسية لإدارة مجموعات TaskPane وWebExtension بكفاءة.
type: docs
weight: 7550
url: /ar/net/aspose.words.webextensions/basewebextensioncollection-1/
---
## BaseWebExtensionCollection&lt;T&gt; class

الفئة الأساسية لـ[`TaskPaneCollection`](../taskpanecollection/) ،[`WebExtensionBindingCollection`](../webextensionbindingcollection/) ، [`WebExtensionPropertyCollection`](../webextensionpropertycollection/) و[`WebExtensionReferenceCollection`](../webextensionreferencecollection/) المجموعات.

لمعرفة المزيد، قم بزيارة[العمل مع الوظائف الإضافية لـ Office](https://docs.aspose.com/words/net/work-with-office-add-ins/) مقالة توثيقية.

```csharp
public abstract class BaseWebExtensionCollection<T> : IEnumerable<T>
    where T : class
```

| معامل | وصف |
| --- | --- |
| T | نوع من عناصر المجموعة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } | يحصل على عنصر أو يعينه في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(*T*) | يضيف العنصر المحدد إلى المجموعة. |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() | يزيل جميع العناصر من المجموعة. |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() | يعيد مُعَدِّدًا يمكنه التكرار خلال مجموعة. |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(*int*) | يزيل العنصر الموجود في الفهرس المحدد من المجموعة. |

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

* مساحة الاسم [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* المجسم [Aspose.Words](../../)
