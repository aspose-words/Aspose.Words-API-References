---
title: CustomPartCollection Class
linktitle: CustomPartCollection
articleTitle: CustomPartCollection
second_title: Aspose.Words لـ .NET
description: استكشف فئة Aspose.Words.Markup.CustomPartCollection لإدارة كائنات CustomPart بكفاءة. حسّن قدراتك في معالجة المستندات اليوم!
type: docs
weight: 4600
url: /ar/net/aspose.words.markup/custompartcollection/
---
## CustomPartCollection class

يمثل مجموعة من[`CustomPart`](../custompart/) الأشياء.

لمعرفة المزيد، قم بزيارة[علامات المستند المنظم أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

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
| [Count](../../aspose.words.markup/custompartcollection/count/) { get; } | يحصل على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.markup/custompartcollection/item/) { get; set; } | يحصل على عنصر أو يعينه في الفهرس المحدد. |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.markup/custompartcollection/add/)(*[CustomPart](../custompart/)*) | يضيف عنصرًا إلى المجموعة. |
| [Clear](../../aspose.words.markup/custompartcollection/clear/)() | يزيل جميع العناصر من المجموعة. |
| [Clone](../../aspose.words.markup/custompartcollection/clone/)() | يقوم بعمل نسخة عميقة من هذه المجموعة وعناصرها. |
| [GetEnumerator](../../aspose.words.markup/custompartcollection/getenumerator/)() | يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة. |
| [RemoveAt](../../aspose.words.markup/custompartcollection/removeat/)(*int*) | يزيل عنصرًا عند الفهرس المحدد. |

## ملاحظات

لا تحتاج عادةً إلى إنشاء مثيلات لهذه الفئة. يمكنك الوصول إلى الأجزاء المخصصة المتعلقة بحزمة OOXML عبر[`PackageCustomParts`](../../aspose.words/document/packagecustomparts/) ملكية.

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

* class [CustomPart](../custompart/)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)
