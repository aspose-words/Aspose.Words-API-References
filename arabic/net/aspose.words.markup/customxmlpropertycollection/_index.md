---
title: Class CustomXmlPropertyCollection
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Markup.CustomXmlPropertyCollection فصل. يمثل مجموعة من سمات XML المخصصة أو خصائص العلامات الذكية.
type: docs
weight: 3950
url: /ar/net/aspose.words.markup/customxmlpropertycollection/
---
## CustomXmlPropertyCollection class

يمثل مجموعة من سمات XML المخصصة أو خصائص العلامات الذكية.

لمعرفة المزيد، قم بزيارة[علامات المستندات المنظمة أو التحكم في المحتوى](https://docs.aspose.com/words/net/working-with-content-control-sdt/) مقالة توثيقية.

```csharp
public class CustomXmlPropertyCollection : IEnumerable<CustomXmlProperty>
```

## الخصائص

| اسم | وصف |
| --- | --- |
| [Count](../../aspose.words.markup/customxmlpropertycollection/count/) { get; } | الحصول على عدد العناصر الموجودة في المجموعة. |
| [Item](../../aspose.words.markup/customxmlpropertycollection/item/) { get; } | الحصول على خاصية بالاسم المحدد. (2 indexers) |

## طُرق

| اسم | وصف |
| --- | --- |
| [Add](../../aspose.words.markup/customxmlpropertycollection/add/)(CustomXmlProperty) | إضافة خاصية إلى المجموعة. |
| [Clear](../../aspose.words.markup/customxmlpropertycollection/clear/)() | إزالة كافة العناصر من المجموعة. |
| [Contains](../../aspose.words.markup/customxmlpropertycollection/contains/)(string) | تحديد ما إذا كانت المجموعة تحتوي على خاصية بالاسم المحدد. |
| [GetEnumerator](../../aspose.words.markup/customxmlpropertycollection/getenumerator/)() | إرجاع كائن العداد الذي يمكن استخدامه للتكرار على كافة العناصر الموجودة في المجموعة. |
| [IndexOfKey](../../aspose.words.markup/customxmlpropertycollection/indexofkey/)(string) | إرجاع الفهرس الصفري للخاصية المحددة في المجموعة. |
| [Remove](../../aspose.words.markup/customxmlpropertycollection/remove/)(string) | إزالة خاصية بالاسم المحدد من المجموعة. |
| [RemoveAt](../../aspose.words.markup/customxmlpropertycollection/removeat/)(int) | إزالة خاصية في الفهرس المحدد. |

### ملاحظات

العناصر هي[`CustomXmlProperty`](../customxmlproperty/) أشياء.

### أمثلة

يوضح كيفية التعامل مع خصائص العلامات الذكية للحصول على معلومات متعمقة حول العلامات الذكية.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// العلامة الذكية التي تظهر في مستند باستخدام Microsoft Word تتعرف على جزء من نصه كشكل من أشكال البيانات،
// مثل الاسم أو التاريخ أو العنوان، وتحويله إلى ارتباط تشعبي يعرض تسطيرًا منقطًا أرجوانيًا.
// في Word 2003، يمكننا تمكين العلامات الذكية عبر "الأدوات" -> "خيارات التصحيح التلقائي..." -> "العلامات الذكية".
// في مستند الإدخال لدينا، هناك ثلاثة كائنات سجلها Microsoft Word كعلامات ذكية.
// قد تكون العلامات الذكية متداخلة، لذا تحتوي هذه المجموعة على المزيد.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// يحتوي عضو "الخصائص" في العلامة الذكية على بيانات التعريف الخاصة به، والتي ستكون مختلفة لكل نوع من أنواع العلامات الذكية.
// تحتوي خصائص العلامة الذكية من نوع "التاريخ" على السنة والشهر واليوم الخاص بها.
CustomXmlPropertyCollection properties = smartTags[7].Properties;

Assert.AreEqual(4, properties.Count);

using (IEnumerator<CustomXmlProperty> enumerator = properties.GetEnumerator())
{
    while (enumerator.MoveNext())
    {
        Console.WriteLine($"Property name: {enumerator.Current.Name}, value: {enumerator.Current.Value}");
        Assert.AreEqual("", enumerator.Current.Uri);
    }
}

// يمكننا أيضًا الوصول إلى الخصائص بطرق مختلفة، مثل زوج المفتاح والقيمة.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// فيما يلي ثلاث طرق لإزالة العناصر من مجموعة الخصائص.
// 1 - الإزالة حسب الفهرس:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - الإزالة بالاسم:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - مسح المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [CustomXmlProperty](../customxmlproperty/)
* مساحة الاسم [Aspose.Words.Markup](../../aspose.words.markup/)
* المجسم [Aspose.Words](../../)


