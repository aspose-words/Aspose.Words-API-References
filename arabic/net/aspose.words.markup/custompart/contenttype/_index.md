---
title: CustomPart.ContentType
linktitle: ContentType
articleTitle: ContentType
second_title: Aspose.Words لـ .NET
description: CustomPart ContentType ملكية. يحدد نوع محتوى هذا الجزء المخصص في C#.
type: docs
weight: 20
url: /ar/net/aspose.words.markup/custompart/contenttype/
---
## CustomPart.ContentType property

يحدد نوع محتوى هذا الجزء المخصص.

```csharp
public string ContentType { get; set; }
```

## ملاحظات

هذه الخاصية قابلة للتطبيق فقط عندما[`IsExternal`](../isexternal/) يكون`خطأ شنيع`.

القيمة الافتراضية هي سلسلة فارغة. يجب أن تكون القيمة الصالحة عبارة عن سلسلة غير فارغة.

## أمثلة

يوضح كيفية الوصول إلى مجموعة الأجزاء المخصصة العشوائية للمستند.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// انسخ الجزء الثاني، ثم أضف النسخة إلى المجموعة.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// قم بتعداد المجموعة وطباعة كل جزء منها.
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

// يمكننا إزالة العناصر من هذه المجموعة بشكل فردي، أو كلها مرة واحدة.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### أنظر أيضا

* class [CustomPart](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
