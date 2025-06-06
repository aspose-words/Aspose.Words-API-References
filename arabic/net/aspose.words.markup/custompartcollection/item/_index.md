---
title: CustomPartCollection.Item
linktitle: Item
articleTitle: Item
second_title: Aspose.Words لـ .NET
description: أدر مجموعة CustomPartCollection الخاصة بك بسهولة باستخدام خاصية العناصر لدينا. احصل على العناصر أو عيّنها بسرعة في أي فهرس لتخصيص سلس وفعال.
type: docs
weight: 30
url: /ar/net/aspose.words.markup/custompartcollection/item/
---
## CustomPartCollection indexer

يحصل على عنصر أو يعينه في الفهرس المحدد.

```csharp
public CustomPart this[int index] { get; set; }
```

| معامل | وصف |
| --- | --- |
| index | مؤشر يعتمد على الصفر للعنصر. |

## أمثلة

يوضح كيفية الوصول إلى مجموعة الأجزاء المخصصة التعسفية للمستند.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

//استنساخ الجزء الثاني، ثم إضافة الاستنساخ إلى المجموعة.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// قم بإحصاء المجموعة وطباعة كل جزء منها.
using (IEnumerator<CustomPart> enumerator = doc.PackageCustomParts.GetEnumerator())
{
    int index = 0;
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Part index {index}:");
        Console.WriteLine($"\tName:\t\t\t\t{enumerator.Current.Name}");
        Console.WriteLine($"\tContent type:\t\t{enumerator.Current.ContentType}");
        Console.WriteLine($"\tRelationship type:\t{enumerator.Current.RelationshipType}");
        Console.WriteLine(enumerator.Current.IsExternal ?
            "\tSourced from outside the document" :
            $"\tStored within the document, length: {enumerator.Current.Data.Length} bytes");
        index++;
    }
}

//يمكننا إزالة العناصر من هذه المجموعة بشكل فردي، أو كلها مرة واحدة.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### أنظر أيضا

* class [CustomPart](../../custompart/)
* class [CustomPartCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
