---
title: Class CustomPartCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Markup.CustomPartCollection فصل. يمثل مجموعة منCustomPart الكائنات.
type: docs
weight: 3910
url: /ar/net/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class

يمثل مجموعة من[`CustomPart`](../custompart/) الكائنات.

لمعرفة المزيد، قم بزيارة[علامات المستندات المنظمة أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class CustomPartCollection : IEnumerable<CustomPart>
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [CustomPartCollection](custompartcollection/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.markup/custompartcollection/count/) { get; } | الحصول على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.markup/custompartcollection/item/) { get; set; } | الحصول على عنصر أو تعيينه في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.markup/custompartcollection/add/)(CustomPart) | إضافة عنصر إلى المجموعة. |
| [Clear](../../aspose.words.markup/custompartcollection/clear/)() | إزالة كافة العناصر من المجموعة. |
| [Clone](../../aspose.words.markup/custompartcollection/clone/)() | عمل نسخة عميقة من هذه المجموعة وعناصرها. |
| [GetEnumerator](../../aspose.words.markup/custompartcollection/getenumerator/)() | إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة. |
| [RemoveAt](../../aspose.words.markup/custompartcollection/removeat/)(int) | إزالة عنصر في الفهرس المحدد. |

### ملاحظات

لا تحتاج عادةً إلى إنشاء مثيلات لهذه الفئة. يمكنك الوصول إلى الأجزاء المخصصة المتعلقة بحزمة OOXML عبر ملف[`PackageCustomParts`](../../aspose.words/document/packagecustomparts/) ملكية.

### أمثلة

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

* class [CustomPart](../custompart/)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)


