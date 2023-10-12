---
title: Odso.RecipientDatas
second_title: Aspose.Words لمراجع .NET API
description: Odso ملكية. الحصول على أو تعيين مجموعة من الكائنات التي تحدد التضمين/الاستبعاد للسجلات الفردية في دمج المراسلات. لا يتم استخدام هذا الكائن أبدًاباطل .
type: docs
weight: 70
url: /ar/net/aspose.words.settings/odso/recipientdatas/
---
## Odso.RecipientDatas property

الحصول على أو تعيين مجموعة من الكائنات التي تحدد التضمين/الاستبعاد للسجلات الفردية في دمج المراسلات. لا يتم استخدام هذا الكائن أبدًا`باطل` .

```csharp
public OdsoRecipientDataCollection RecipientDatas { get; set; }
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

* class [OdsoRecipientDataCollection](../../odsorecipientdatacollection/)
* class [Odso](../)
* مساحة الاسم [Aspose.Words.Settings](../../odso/)
* المجسم [Aspose.Words](../../../)


