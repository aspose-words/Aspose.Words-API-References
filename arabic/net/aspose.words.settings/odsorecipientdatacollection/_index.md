---
title: Class OdsoRecipientDataCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.OdsoRecipientDataCollection فصل. مجموعة مطبوعة منOdsoRecipientData
type: docs
weight: 5940
url: /ar/net/aspose.words.settings/odsorecipientdatacollection/
---
## OdsoRecipientDataCollection class

مجموعة مطبوعة من[`OdsoRecipientData`](../odsorecipientdata/)

لمعرفة المزيد، قم بزيارة[دمج البريد وإعداد التقارير](https://docs.aspose.com/words/net/mail-merge-and-reporting/) مقالة توثيقية.

```csharp
public class OdsoRecipientDataCollection : IEnumerable<OdsoRecipientData>
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [OdsoRecipientDataCollection](odsorecipientdatacollection/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.settings/odsorecipientdatacollection/count/) { get; } | الحصول على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.settings/odsorecipientdatacollection/item/) { get; set; } | الحصول على أو تعيين عنصر في هذه المجموعة. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.settings/odsorecipientdatacollection/add/)(OdsoRecipientData) | إضافة كائن إلى نهاية هذه المجموعة. |
| [Clear](../../aspose.words.settings/odsorecipientdatacollection/clear/)() | إزالة كافة العناصر من هذه المجموعة. |
| [GetEnumerator](../../aspose.words.settings/odsorecipientdatacollection/getenumerator/)() | إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة. |
| [RemoveAt](../../aspose.words.settings/odsorecipientdatacollection/removeat/)(int) | إزالة العنصر الموجود في الفهرس المحدد. |

### أمثلة

يوضح كيفية الوصول إلى مجموعة البيانات التي تحدد سجلات مصدر بيانات الدمج التي سيتم استبعادها من خلال دمج البريد.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

OdsoRecipientDataCollection dataCollection = doc.MailMergeSettings.Odso.RecipientDatas;

Assert.AreEqual(70, dataCollection.Count);

using (IEnumerator<OdsoRecipientData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine(
            $"Odso recipient data index {index++} will {(enumerator.Current.Active ? "" : "not ")}be imported upon mail merge.");
        Console.WriteLine($"\tColumn #{enumerator.Current.Column}");
        Console.WriteLine($"\tHash code: {enumerator.Current.Hash}");
        Console.WriteLine($"\tContents array length: {enumerator.Current.UniqueTag.Length}");
    }
}

// يمكننا استنساخ العناصر الموجودة في هذه المجموعة.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// يمكننا أيضًا إزالة العناصر بشكل فردي، أو مسح المجموعة بأكملها مرة واحدة.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### أنظر أيضا

* class [OdsoRecipientData](../odsorecipientdata/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)


