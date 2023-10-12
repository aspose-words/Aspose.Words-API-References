---
title: Class BaseWebExtensionCollectionT
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.WebExtensions.BaseWebExtensionCollection1T فصل. الفئة الأساسية لـTaskPaneCollection WebExtensionBindingCollectionWebExtensionPropertyCollection وWebExtensionReferenceCollection المجموعات.
type: docs
weight: 6700
url: /ar/net/aspose.words.webextensions/basewebextensioncollection-1/
---
## BaseWebExtensionCollection&lt;T&gt; class

الفئة الأساسية لـ[`TaskPaneCollection`](../taskpanecollection/) ,[`WebExtensionBindingCollection`](../webextensionbindingcollection/)[`WebExtensionPropertyCollection`](../webextensionpropertycollection/) و[`WebExtensionReferenceCollection`](../webextensionreferencecollection/) المجموعات.

لمعرفة المزيد، قم بزيارة[العمل مع وظائف Office الإضافية](https://docs.aspose.com/words/net/work-with-office-add-ins/) مقالة توثيقية.

```csharp
public abstract class BaseWebExtensionCollection<T> : IEnumerable<T>
    where T : class
```

| معامل | وصف |
| --- | --- |
| T | نوع عنصر المجموعة. |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.webextensions/basewebextensioncollection-1/count/) { get; } | الحصول على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.webextensions/basewebextensioncollection-1/item/) { get; set; } | الحصول على عنصر أو تعيينه في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.webextensions/basewebextensioncollection-1/add/)(T) | إضافة عنصر محدد إلى المجموعة. |
| [Clear](../../aspose.words.webextensions/basewebextensioncollection-1/clear/)() | إزالة كافة العناصر من المجموعة. |
| [GetEnumerator](../../aspose.words.webextensions/basewebextensioncollection-1/getenumerator/)() | يُرجع عدادًا يمكنه التكرار من خلال مجموعة. |
| [Remove](../../aspose.words.webextensions/basewebextensioncollection-1/remove/)(int) | إزالة العنصر الموجود في الفهرس المحدد من المجموعة. |

### أمثلة

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

* مساحة الاسم [Aspose.Words.WebExtensions](../../aspose.words.webextensions/)
* المجسم [Aspose.Words](../../)


