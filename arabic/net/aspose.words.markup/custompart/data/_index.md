---
title: CustomPart.Data
linktitle: Data
articleTitle: Data
second_title: Aspose.Words لـ .NET
description: استكشف بيانات CustomPart. احصل على معلومات مفصلة حول قطعك المخصصة لتحسين الدقة والكفاءة في مشاريعك.
type: docs
weight: 30
url: /ar/net/aspose.words.markup/custompart/data/
---
## CustomPart.Data property

يحتوي على بيانات هذا الجزء المخصص.

```csharp
public byte[] Data { get; set; }
```

## ملاحظات

تنطبق هذه الخاصية فقط عندما[`IsExternal`](../isexternal/) يكون`خطأ شنيع`.

القيمة الافتراضية هي مصفوفة بايتات فارغة. لا يمكن استخدام القيمة`باطل`.

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

* class [CustomPart](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
