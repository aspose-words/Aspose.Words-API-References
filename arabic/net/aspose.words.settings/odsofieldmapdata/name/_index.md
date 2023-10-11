---
title: OdsoFieldMapData.Name
second_title: Aspose.Words لمراجع .NET API
description: OdsoFieldMapData ملكية. يحدد اسم العمود ضمن مصدر بيانات خارجي للعمود الذي تم تحديد فهرسه بواسطةColumnproperty. القيمة الافتراضية هي سلسلة فارغة.
type: docs
weight: 40
url: /ar/net/aspose.words.settings/odsofieldmapdata/name/
---
## OdsoFieldMapData.Name property

يحدد اسم العمود ضمن مصدر بيانات خارجي للعمود الذي تم تحديد فهرسه بواسطة[`Column`](../column/)property. القيمة الافتراضية هي سلسلة فارغة.

```csharp
public string Name { get; set; }
```

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

* class [OdsoFieldMapData](../)
* مساحة الاسم [Aspose.Words.Settings](../../odsofieldmapdata/)
* المجسم [Aspose.Words](../../../)


