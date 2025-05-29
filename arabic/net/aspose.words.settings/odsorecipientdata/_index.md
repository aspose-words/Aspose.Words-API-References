---
title: OdsoRecipientData Class
linktitle: OdsoRecipientData
articleTitle: OdsoRecipientData
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.Settings.OdsoRecipientData، المصممة لإدارة واستبعاد سجلات معينة في عمليات دمج البريد من أجل معالجة المستندات بكفاءة.
type: docs
weight: 6760
url: /ar/net/aspose.words.settings/odsorecipientdata/
---
## OdsoRecipientData class

يمثل معلومات حول سجل واحد ضمن مصدر بيانات خارجي يجب استبعاده من دمج البريد.

لمعرفة المزيد، قم بزيارة[دمج البريد وإعداد التقارير](https://docs.aspose.com/words/net/mail-merge-and-reporting/) مقالة توثيقية.

```csharp
public class OdsoRecipientData
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [OdsoRecipientData](odsorecipientdata/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Active](../../aspose.words.settings/odsorecipientdata/active/) { get; set; } | يحدد ما إذا كان سيتم استيراد السجل من مصدر البيانات إلى مستند عند تنفيذ دمج البريد. القيمة الافتراضية هي`حقيقي` . |
| [Column](../../aspose.words.settings/odsorecipientdata/column/) { get; set; } | يحدد العمود داخل مصدر البيانات الذي يحتوي على بيانات فريدة للسجل الحالي. القيمة الافتراضية هي 0. |
| [Hash](../../aspose.words.settings/odsorecipientdata/hash/) { get; set; } | يمثل رمز التجزئة لهذا السجل. في بعض الأحيان يستخدم Microsoft Word[`Hash`](./hash/) من سجل كامل بدلا من[`UniqueTag`](./uniquetag/) القيمة الافتراضية هي 0. |
| [UniqueTag](../../aspose.words.settings/odsorecipientdata/uniquetag/) { get; set; } | يحدد محتويات سجل معين في العمود الذي يحتوي على بيانات فريدة. القيمة الافتراضية هي`باطل` . |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.settings/odsorecipientdata/clone/)() | يعيد نسخة طبق الأصل من هذا الكائن. |

## ملاحظات

إذا تم دمج سجل في مستند مدمج، فلن تكون هناك حاجة إلى أي معلومات حول هذا السجل. ومع ذلك، إذا لم يتم دمج سجل معين في مستند مدمج، فسيتم تخزين قيمة المفتاح الفريد لهذا السجل في[`UniqueTag`](./uniquetag/)خاصية هذا الكائن للإشارة إلى هذا الاستبعاد.

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

* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
