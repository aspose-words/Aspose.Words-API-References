---
title: Enum OdsoFieldMappingType
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Settings.OdsoFieldMappingType تعداد. يحدد الأنواع المحتملة المستخدمة للإشارة إلى ما إذا كان حقل دمج البريد المحدد قد تم تعيينه إلى عمود في مصدر البيانات الخارجي المحدد.
type: docs
weight: 5920
url: /ar/net/aspose.words.settings/odsofieldmappingtype/
---
## OdsoFieldMappingType enumeration

يحدد الأنواع المحتملة المستخدمة للإشارة إلى ما إذا كان حقل دمج البريد المحدد قد تم تعيينه إلى عمود في مصدر البيانات الخارجي المحدد.

```csharp
public enum OdsoFieldMappingType
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Column | `0` | تحديد أنه تم تعيين حقل دمج البريد إلى عمود في مصدر البيانات الخارجي المحدد. |
| Null | `1` | تحديد أنه لم يتم تعيين حقل دمج البريد إلى عمود في مصدر البيانات الخارجي المحدد. |
| Default | `1` | يساويNull . |

### أمثلة

يوضح كيفية الوصول إلى مجموعة البيانات التي تقوم بتعيين أعمدة مصدر البيانات لدمج الحقول.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// تحدد هذه المجموعة كيفية تعيين دمج البريد للأعمدة من مصدر بيانات
// لحقول MERGEFIELD وADDRESSBLOCK وGREETINGLINE المحددة مسبقًا.
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

// استنساخ العناصر الموجودة في هذه المجموعة.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// استخدم عناصر الطريقة "RemoveAt" بشكل فردي حسب الفهرس.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// استخدم طريقة "مسح" لمسح المجموعة بأكملها مرة واحدة.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### أنظر أيضا

* property [Type](../odsofieldmapdata/type/)
* مساحة الاسم [Aspose.Words.Settings](../../aspose.words.settings/)
* المجسم [Aspose.Words](../../)


