---
title: OdsoFieldMappingType Enum
linktitle: OdsoFieldMappingType
articleTitle: OdsoFieldMappingType
second_title: Aspose.Words لـ .NET
description: اكتشف Aspose.Words.OdsoFieldMappingType enum لربط حقول دمج البريد بكفاءة مع مصادر البيانات الخارجية. حسّن أتمتة مستنداتك اليوم!
type: docs
weight: 6750
url: /ar/net/aspose.words.settings/odsofieldmappingtype/
---
## OdsoFieldMappingType enumeration

يحدد الأنواع الممكنة المستخدمة للإشارة إلى ما إذا كان حقل دمج البريد المحدد قد تم تعيينه إلى عمود في مصدر البيانات الخارجي المحدد.

```csharp
public enum OdsoFieldMappingType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Column | `0` | يحدد أن حقل دمج البريد تم تعيينه إلى عمود في مصدر البيانات الخارجي المحدد. |
| Null | `1` | يحدد أن حقل دمج البريد لم يتم تعيينه إلى عمود في مصدر البيانات الخارجي المحدد. |
| Default | `1` | يساويNull . |

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

* property [Type](../odsofieldmapdata/type/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)
