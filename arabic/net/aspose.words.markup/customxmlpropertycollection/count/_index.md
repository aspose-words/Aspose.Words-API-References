---
title: CustomXmlPropertyCollection.Count
second_title: Aspose.Words لمراجع .NET API
description: CustomXmlPropertyCollection ملكية. الحصول على عدد العناصر الموجودة في المجموعة.
type: docs
weight: 10
url: /ar/net/aspose.words.markup/customxmlpropertycollection/count/
---
## CustomXmlPropertyCollection.Count property

الحصول على عدد العناصر الموجودة في المجموعة.

```csharp
public int Count { get; }
```

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

* class [CustomXmlPropertyCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../customxmlpropertycollection/)
* المجسم [Aspose.Words](../../../)


