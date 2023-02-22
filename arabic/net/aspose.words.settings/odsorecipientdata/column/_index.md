---
title: OdsoRecipientData.Column
second_title: Aspose.Words لمراجع .NET API
description: OdsoRecipientData ملكية. يحدد العمود داخل مصدر البيانات الذي يحتوي على بيانات فريدة للسجل الحالي. القيمة الافتراضية هي 0.
type: docs
weight: 30
url: /ar/net/aspose.words.settings/odsorecipientdata/column/
---
## OdsoRecipientData.Column property

يحدد العمود داخل مصدر البيانات الذي يحتوي على بيانات فريدة للسجل الحالي. القيمة الافتراضية هي 0.

```csharp
public int Column { get; set; }
```

### أمثلة

يوضح كيفية الوصول إلى مجموعة البيانات التي تحدد سجلات مصدر بيانات الدمج التي سيستبعدها دمج المراسلات.

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

// يمكننا استنساخ العناصر في هذه المجموعة.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// يمكننا أيضًا إزالة العناصر بشكل فردي ، أو مسح المجموعة بأكملها مرة واحدة.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### أنظر أيضا

* class [OdsoRecipientData](../)
* مساحة الاسم [Aspose.Words.Settings](../../odsorecipientdata/)
* المجسم [Aspose.Words](../../../)


