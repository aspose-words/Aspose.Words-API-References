---
title: CustomPart.RelationshipType
second_title: Aspose.Words لمراجع .NET API
description: CustomPart ملكية. الحصول على نوع العلاقة أو تعيينه من الجزء الأصل إلى هذا الجزء المخصص.
type: docs
weight: 60
url: /ar/net/aspose.words.markup/custompart/relationshiptype/
---
## CustomPart.RelationshipType property

الحصول على نوع العلاقة أو تعيينه من الجزء الأصل إلى هذا الجزء المخصص.

```csharp
public string RelationshipType { get; set; }
```

### ملاحظات

يجب أن يكون نوع العلاقة للجزء المخصص "غير معروف" ، على سبيل المثال ، نوع العلاقة المخصص ، وليس أحد أنواع العلاقات المحددة في ISO / IEC 29500.

القيمة الافتراضية هي سلسلة فارغة. يجب أن تكون القيمة الصالحة سلسلة غير فارغة.

### أمثلة

يوضح كيفية الوصول إلى مجموعة الأجزاء المخصصة التعسفية للمستند.

```csharp
Document doc = new Document(MyDir + "Custom parts OOXML package.docx");

Assert.AreEqual(2, doc.PackageCustomParts.Count);

// استنساخ الجزء الثاني ، ثم أضف النسخة إلى المجموعة.
CustomPart clonedPart = doc.PackageCustomParts[1].Clone();
doc.PackageCustomParts.Add(clonedPart);
Assert.AreEqual(3, doc.PackageCustomParts.Count);

// تعداد المجموعة وطباعة كل جزء.
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

// يمكننا إزالة العناصر من هذه المجموعة بشكل فردي أو كلها مرة واحدة.
doc.PackageCustomParts.RemoveAt(2);

Assert.AreEqual(2, doc.PackageCustomParts.Count);

doc.PackageCustomParts.Clear();

Assert.AreEqual(0, doc.PackageCustomParts.Count);
```

### أنظر أيضا

* class [CustomPart](../)
* مساحة الاسم [Aspose.Words.Markup](../../custompart/)
* المجسم [Aspose.Words](../../../)


