---
title: Item
second_title: Aspose.Words لمراجع .NET API
description: الحصول على خاصية بالاسم المحدد .
type: docs
weight: 20
url: /ar/net/aspose.words.markup/customxmlpropertycollection/item/
---
## CustomXmlPropertyCollection indexer (1 of 2)

الحصول على خاصية بالاسم المحدد .

```csharp
public CustomXmlProperty this[string name] { get; }
```

| معامل | وصف |
| --- | --- |
| name | اسم حساس لحالة الأحرف للخاصية المراد تحديد موقعها. |

### أمثلة

يوضح كيفية استخدام خصائص العلامات الذكية للحصول على معلومات متعمقة حول العلامات الذكية.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// تظهر علامة ذكية في مستند مع Microsoft Word يتعرف على جزء من نصه كشكل من أشكال البيانات ،
// مثل الاسم أو التاريخ أو العنوان ، ويحوله إلى ارتباط تشعبي يعرض تسطيرًا منقطًا بنفسجي اللون.
// في Word 2003 ، يمكننا تمكين العلامات الذكية عبر "Tools" - > "خيارات التصحيح التلقائي ..." - >. "العلامات الذكية".
// في مستند الإدخال لدينا ، هناك ثلاثة كائنات سجلها Microsoft Word كعلامات ذكية.
// قد تكون العلامات الذكية متداخلة ، لذا تحتوي هذه المجموعة على المزيد.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// يحتوي عضو "الخصائص" للعلامة الذكية على البيانات الوصفية الخاصة بها ، والتي ستكون مختلفة لكل نوع من أنواع العلامات الذكية.
// تحتوي خصائص العلامة الذكية من نوع "التاريخ" على السنة والشهر واليوم.
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

// يمكننا أيضًا الوصول إلى الخصائص بطرق مختلفة ، مثل زوج المفتاح والقيمة.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// فيما يلي ثلاث طرق لإزالة العناصر من مجموعة الخصائص.
// 1 - إزالة حسب الفهرس:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - إزالة بالاسم:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - امسح المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [CustomXmlProperty](../../customxmlproperty)
* class [CustomXmlPropertyCollection](../../customxmlpropertycollection)
* مساحة الاسم [Aspose.Words.Markup](../../customxmlpropertycollection)
* المجسم [Aspose.Words](../../../)

---

## CustomXmlPropertyCollection indexer (2 of 2)

يحصل على خاصية في الفهرس المحدد .

```csharp
public CustomXmlProperty this[int index] { get; }
```

| معامل | وصف |
| --- | --- |
| index | فهرس للممتلكات على أساس الصفر. |

### أمثلة

يوضح كيفية استخدام خصائص العلامات الذكية للحصول على معلومات متعمقة حول العلامات الذكية.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// تظهر علامة ذكية في مستند مع Microsoft Word يتعرف على جزء من نصه كشكل من أشكال البيانات ،
// مثل الاسم أو التاريخ أو العنوان ، ويحوله إلى ارتباط تشعبي يعرض تسطيرًا منقطًا بنفسجي اللون.
// في Word 2003 ، يمكننا تمكين العلامات الذكية عبر "Tools" - > "خيارات التصحيح التلقائي ..." - >. "العلامات الذكية".
// في مستند الإدخال لدينا ، هناك ثلاثة كائنات سجلها Microsoft Word كعلامات ذكية.
// قد تكون العلامات الذكية متداخلة ، لذا تحتوي هذه المجموعة على المزيد.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// يحتوي عضو "الخصائص" للعلامة الذكية على البيانات الوصفية الخاصة بها ، والتي ستكون مختلفة لكل نوع من أنواع العلامات الذكية.
// تحتوي خصائص العلامة الذكية من نوع "التاريخ" على السنة والشهر واليوم.
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

// يمكننا أيضًا الوصول إلى الخصائص بطرق مختلفة ، مثل زوج المفتاح والقيمة.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// فيما يلي ثلاث طرق لإزالة العناصر من مجموعة الخصائص.
// 1 - إزالة حسب الفهرس:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - إزالة بالاسم:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - امسح المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [CustomXmlProperty](../../customxmlproperty)
* class [CustomXmlPropertyCollection](../../customxmlpropertycollection)
* مساحة الاسم [Aspose.Words.Markup](../../customxmlpropertycollection)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
