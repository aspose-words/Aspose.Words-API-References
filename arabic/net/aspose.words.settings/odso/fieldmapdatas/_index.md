---
title: Odso.FieldMapDatas
linktitle: FieldMapDatas
articleTitle: FieldMapDatas
second_title: Aspose.Words لـ .NET
description: Odso FieldMapDatas ملكية. الحصول على أو تعيين مجموعة من الكائنات التي تحدد كيفية تعيين الأعمدة من مصدر البيانات الخارجي إلى أسماء حقول الدمج المحددة مسبقًا في المستند. لا يتم استخدام هذا الكائن أبدًاباطل  في C#.
type: docs
weight: 50
url: /ar/net/aspose.words.settings/odso/fieldmapdatas/
---
## Odso.FieldMapDatas property

الحصول على أو تعيين مجموعة من الكائنات التي تحدد كيفية تعيين الأعمدة من مصدر البيانات الخارجي إلى أسماء حقول الدمج المحددة مسبقًا في المستند. لا يتم استخدام هذا الكائن أبدًا`باطل` .

```csharp
public OdsoFieldMapDataCollection FieldMapDatas { get; set; }
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

* class [OdsoFieldMapDataCollection](../../odsofieldmapdatacollection/)
* class [Odso](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
