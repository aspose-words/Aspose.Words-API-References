---
title: CustomPart.RelationshipType
linktitle: RelationshipType
articleTitle: RelationshipType
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية CustomPart RelationshipType لإدارة العلاقات وتحديدها بسهولة بين الأجزاء الأصلية والأجزاء المخصصة لتحسين الوظائف.
type: docs
weight: 60
url: /ar/net/aspose.words.markup/custompart/relationshiptype/
---
## CustomPart.RelationshipType property

يحصل على نوع العلاقة من الجزء الرئيسي إلى هذا الجزء المخصص أو يعينه.

```csharp
public string RelationshipType { get; set; }
```

## ملاحظات

يجب أن يكون نوع العلاقة للجزء المخصص "غير معروف"، على سبيل المثال نوع علاقة مخصصة، وليس أحد أنواع العلاقات المحددة ضمن ISO/IEC 29500.

القيمة الافتراضية هي سلسلة نصية فارغة. يجب أن تكون القيمة الصحيحة سلسلة نصية غير فارغة.

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
