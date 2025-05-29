---
title: OdsoFieldMapData Class
linktitle: OdsoFieldMapData
articleTitle: OdsoFieldMapData
second_title: Aspose.Words لـ .NET
description: اكتشف فئة Aspose.Words.OdsoFieldMapData لربط أعمدة البيانات الخارجية بسلاسة بحقول دمج المستندات المحددة مسبقًا، مما يعزز أتمتة المستندات لديك.
type: docs
weight: 6730
url: /ar/net/aspose.words.settings/odsofieldmapdata/
---
## OdsoFieldMapData class

يحدد كيفية تعيين عمود في مصدر البيانات الخارجي إلى حقول الدمج المحددة مسبقًا داخل المستند.

لمعرفة المزيد، قم بزيارة[دمج البريد وإعداد التقارير](https://docs.aspose.com/words/net/mail-merge-and-reporting/) مقالة توثيقية.

```csharp
public class OdsoFieldMapData
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [OdsoFieldMapData](odsofieldmapdata/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Column](../../aspose.words.settings/odsofieldmapdata/column/) { get; set; } | يحدد الفهرس الصفري للعمود داخل مصدر بيانات خارجي والذي يجب أن يكون مطابقًا للاسم المحلي لحقل MERGEFIELD محدد. القيمة الافتراضية هي 0. |
| [MappedName](../../aspose.words.settings/odsofieldmapdata/mappedname/) { get; set; } | يحدد اسم حقل الدمج المحدد مسبقًا والذي يجب تعيينه إلى رقم العمود المحدد بواسطة[`Column`](./column/) الخاصية داخل هذا الحقل mapping. القيمة الافتراضية هي سلسلة فارغة. |
| [Name](../../aspose.words.settings/odsofieldmapdata/name/) { get; set; } | يحدد اسم العمود داخل مصدر بيانات خارجي للعمود الذي تم تحديد فهرسه بواسطة[`Column`](./column/)property. القيمة الافتراضية هي سلسلة فارغة. |
| [Type](../../aspose.words.settings/odsofieldmapdata/type/) { get; set; } | يحدد ما إذا كان حقل دمج البريد المحدد قد تم تعيينه إلى عمود في مصدر البيانات الخارجي المحدد أم لا. القيمة الافتراضية هيDefault . |

## طُرق

| اسم | وصف |
| --- | --- |
| [Clone](../../aspose.words.settings/odsofieldmapdata/clone/)() | يعيد نسخة طبق الأصل من هذا الكائن. |

## ملاحظات

يوفر مايكروسوفت وورد بعض أسماء حقول الدمج المُعرّفة مسبقًا، والتي تسمح بإدراجها في مستند، مثل استخدام MERGEFIELD أو في حقلي ADDRESSBLOCK أو GREETINGLINE. المعلومات المحددة في`OdsoFieldMapData`يسمح لك بتعيين عمود واحد في مصدر البيانات الخارجي إلى حقل دمج محدد مسبقًا.

## أمثلة

يوضح كيفية الوصول إلى مجموعة البيانات التي تقوم بتعيين أعمدة مصدر البيانات إلى حقول الدمج.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// تحدد هذه المجموعة كيفية قيام دمج البريد بتعيين الأعمدة من مصدر البيانات
// إلى الحقول المحددة مسبقًا MERGEFIELD وADDRESSBLOCK وGREETINGLINE.
OdsoFieldMapDataCollection dataCollection = doc.MailMergeSettings.Odso.FieldMapDatas;
Assert.AreEqual(30, dataCollection.Count);

using (IEnumerator<OdsoFieldMapData> enumerator = dataCollection.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Field map data index {index++}, type \"{enumerator.Current.Type}\":");

        Console.WriteLine(
            enumerator.Current.Type != OdsoFieldMappingType.Null
                ? $"\tColumn \"{enumerator.Current.Name}\", number {enumerator.Current.Column} mapped to merge field \"{enumerator.Current.MappedName}\"."
                : "\tNo valid column to field mapping data present.");
    }
}

//استنساخ العناصر في هذه المجموعة.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// استخدم عناصر طريقة "RemoveAt" بشكل فردي حسب الفهرس.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

//استخدم طريقة "المسح" لمسح المجموعة بأكملها مرة واحدة.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
