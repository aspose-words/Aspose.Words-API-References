---
title: OdsoFieldMapDataCollection.Clear
second_title: Aspose.Words لمراجع .NET API
description: OdsoFieldMapDataCollection طريقة. يزيل كل العناصر من هذه المجموعة.
type: docs
weight: 50
url: /ar/net/aspose.words.settings/odsofieldmapdatacollection/clear/
---
## OdsoFieldMapDataCollection.Clear method

يزيل كل العناصر من هذه المجموعة.

```csharp
public void Clear()
```

### أمثلة

يوضح كيفية الوصول إلى مجموعة البيانات التي تعين أعمدة مصدر البيانات لدمج الحقول.

```csharp
Document doc = new Document(MyDir + "Odso data.docx");

// تحدد هذه المجموعة كيف سيقوم دمج البريد بتعيين أعمدة من مصدر بيانات
// إلى حقول MERGEFIELD و ADDRESSBLOCK و GREETINGLINE المحددة مسبقًا.
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

// استنساخ العناصر في هذه المجموعة.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// استخدم عناصر طريقة "RemoveAt" بشكل فردي عن طريق الفهرس.
dataCollection.RemoveAt(0);

Assert.AreEqual(29, dataCollection.Count);

// استخدم طريقة "المسح" لمسح المجموعة بأكملها مرة واحدة.
dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### أنظر أيضا

* class [OdsoFieldMapDataCollection](../)
* مساحة الاسم [Aspose.Words.Settings](../../odsofieldmapdatacollection/)
* المجسم [Aspose.Words](../../../)


