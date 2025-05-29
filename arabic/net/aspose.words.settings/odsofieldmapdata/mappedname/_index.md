---
title: OdsoFieldMapData.MappedName
linktitle: MappedName
articleTitle: MappedName
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية OdsoFieldMapData MappedName، التي تربط أسماء حقول الدمج بالأعمدة المحددة، مما يعزز كفاءة تعيين البيانات ودقتها.
type: docs
weight: 30
url: /ar/net/aspose.words.settings/odsofieldmapdata/mappedname/
---
## OdsoFieldMapData.MappedName property

يحدد اسم حقل الدمج المحدد مسبقًا والذي يجب تعيينه إلى رقم العمود المحدد بواسطة[`Column`](../column/) الخاصية داخل هذا الحقل mapping. القيمة الافتراضية هي سلسلة فارغة.

```csharp
public string MappedName { get; set; }
```

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

* class [OdsoFieldMapData](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
