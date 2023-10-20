---
title: OdsoFieldMapData.Column
linktitle: Column
articleTitle: Column
second_title: Aspose.Words لـ .NET
description: OdsoFieldMapData Column ملكية. يحدد الفهرس الصفري للعمود داخل مصدر بيانات خارجي والذي يجب أن يتم تعيينه إلى الاسم المحلي لحقل MERGEFIELD محدد. القيمة الافتراضية هي 0 في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.settings/odsofieldmapdata/column/
---
## OdsoFieldMapData.Column property

يحدد الفهرس الصفري للعمود داخل مصدر بيانات خارجي والذي يجب أن يتم تعيينه إلى الاسم المحلي لحقل MERGEFIELD محدد. القيمة الافتراضية هي 0.

```csharp
public int Column { get; set; }
```

## أمثلة

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
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
