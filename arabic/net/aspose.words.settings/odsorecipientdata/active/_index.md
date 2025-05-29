---
title: OdsoRecipientData.Active
linktitle: Active
articleTitle: Active
second_title: Aspose.Words لـ .NET
description: تحكم في عمليات استيراد دمج البريد باستخدام خاصية OdsoRecipientData Active. أدر سجلات البيانات بسهولة لإنشاء مستندات بسلاسة. الإعداد الافتراضي هو "صحيح".
type: docs
weight: 20
url: /ar/net/aspose.words.settings/odsorecipientdata/active/
---
## OdsoRecipientData.Active property

يحدد ما إذا كان سيتم استيراد السجل من مصدر البيانات إلى مستند عند تنفيذ دمج البريد. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool Active { get; set; }
```

## أمثلة

يوضح كيفية الوصول إلى مجموعة البيانات التي تحدد سجلات مصدر بيانات الدمج التي سيتم استبعادها من خلال عملية دمج البريد.

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

//يمكننا استنساخ العناصر الموجودة في هذه المجموعة.
Assert.AreNotEqual(dataCollection[0], dataCollection[0].Clone());

//يمكننا أيضًا إزالة العناصر بشكل فردي، أو مسح المجموعة بأكملها مرة واحدة.
dataCollection.RemoveAt(0);

Assert.AreEqual(69, dataCollection.Count);

dataCollection.Clear();

Assert.AreEqual(0, dataCollection.Count);
```

### أنظر أيضا

* class [OdsoRecipientData](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
