---
title: OdsoRecipientDataCollection Class
linktitle: OdsoRecipientDataCollection
articleTitle: OdsoRecipientDataCollection
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.Settings.OdsoRecipientDataCollection، وهي مجموعة مكتوبة قوية لإدارة OdsoRecipientData بكفاءة في تطبيقاتك.
type: docs
weight: 6770
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
| [Count](../../aspose.words.settings/odsorecipientdatacollection/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.settings/odsorecipientdatacollection/item/) { get; set; } | يحصل على عنصر في هذه المجموعة أو يعينه. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.settings/odsorecipientdatacollection/add/)(*[OdsoRecipientData](../odsorecipientdata/)*) | يضيف كائنًا إلى نهاية هذه المجموعة. |
| [Clear](../../aspose.words.settings/odsorecipientdatacollection/clear/)() | يزيل جميع العناصر من هذه المجموعة. |
| [GetEnumerator](../../aspose.words.settings/odsorecipientdatacollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة. |
| [RemoveAt](../../aspose.words.settings/odsorecipientdatacollection/removeat/)(*int*) | يزيل العنصر عند الفهرس المحدد. |

## أمثلة

يوضح كيفية الوصول إلى مجموعة البيانات التي تحدد سجلات مصدر بيانات الدمج التي سيتم استبعادها من خلال عملية دمج البريد.

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

//يمكننا استنساخ العناصر الموجودة في هذه المجموعة.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

//يمكننا أيضًا إزالة العناصر بشكل فردي، أو مسح المجموعة بأكملها مرة واحدة.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### أنظر أيضا

* class [OdsoRecipientData](../odsorecipientdata/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
