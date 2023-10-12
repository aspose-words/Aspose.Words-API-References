---
title: OdsoRecipientData.Hash
second_title: Aspose.Words لمراجع .NET API
description: OdsoRecipientData ملكية. يمثل رمز التجزئة لهذا السجل. يستخدم Microsoft Word أحيانًاHash من سجل كامل بدلا منUniqueTag value. القيمة الافتراضية هي 0.
type: docs
weight: 40
url: /ar/net/aspose.words.settings/odsorecipientdata/hash/
---
## OdsoRecipientData.Hash property

يمثل رمز التجزئة لهذا السجل. يستخدم Microsoft Word أحيانًا`Hash` من سجل كامل بدلا من[`UniqueTag`](../uniquetag/) value. القيمة الافتراضية هي 0.

```csharp
public int Hash { get; set; }
```

### أمثلة

يوضح كيفية الوصول إلى مجموعة البيانات التي تحدد سجلات مصدر بيانات الدمج التي سيتم استبعادها من خلال دمج البريد.

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

// يمكننا استنساخ العناصر الموجودة في هذه المجموعة.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

// يمكننا أيضًا إزالة العناصر بشكل فردي، أو مسح المجموعة بأكملها مرة واحدة.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### أنظر أيضا

* class [OdsoRecipientData](../)
* مساحة الاسم [Aspose.Words.Settings](../../odsorecipientdata/)
* المجسم [Aspose.Words](../../../)


