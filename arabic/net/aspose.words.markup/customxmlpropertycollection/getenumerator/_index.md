---
title: CustomXmlPropertyCollection.GetEnumerator
linktitle: GetEnumerator
articleTitle: GetEnumerator
second_title: Aspose.Words لـ .NET
description: اكتشف طريقة CustomXmlPropertyCollection GetEnumerator للتنقل بسهولة عبر عناصر المجموعة، مما يعزز كفاءة إدارة البيانات لديك.
type: docs
weight: 60
url: /ar/net/aspose.words.markup/customxmlpropertycollection/getenumerator/
---
## CustomXmlPropertyCollection.GetEnumerator method

يعيد كائن عداد يمكن استخدامه للتكرار على جميع العناصر في المجموعة.

```csharp
public IEnumerator<CustomXmlProperty> GetEnumerator()
```

## أمثلة

يوضح كيفية العمل مع خصائص العلامات الذكية للحصول على معلومات متعمقة حول العلامات الذكية.

```csharp
Document doc = new Document(MyDir + "Smart tags.doc");

// تظهر علامة ذكية في مستند باستخدام Microsoft Word تتعرف على جزء من نصه كنوع من البيانات،
// مثل الاسم أو التاريخ أو العنوان، وتحويله إلى ارتباط تشعبي يعرض خطًا منقطًا باللون الأرجواني.
// في Word 2003، يمكننا تمكين العلامات الذكية عبر "أدوات" -> "خيارات التصحيح التلقائي..." -> "العلامات الذكية".
// في مستند الإدخال الخاص بنا، هناك ثلاثة كائنات سجلها Microsoft Word كعلامات ذكية.
//قد تكون العلامات الذكية متداخلة، لذا تحتوي هذه المجموعة على المزيد منها.
SmartTag[] smartTags = doc.GetChildNodes(NodeType.SmartTag, true).OfType<SmartTag>().ToArray();

Assert.AreEqual(8, smartTags.Length);

// يحتوي عنصر "الخصائص" في العلامة الذكية على بياناتها الوصفية، والتي ستكون مختلفة لكل نوع من أنواع العلامات الذكية.
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

//يمكننا أيضًا الوصول إلى الخصائص بطرق مختلفة، مثل زوج المفتاح والقيمة.
Assert.True(properties.Contains("Day"));
Assert.AreEqual("22", properties["Day"].Value);
Assert.AreEqual("2003", properties[2].Value);
Assert.AreEqual(1, properties.IndexOfKey("Month"));

// فيما يلي ثلاث طرق لإزالة العناصر من مجموعة الخصائص.
// 1 - الإزالة حسب الفهرس:
properties.RemoveAt(3);

Assert.AreEqual(3, properties.Count);

// 2 - إزالة حسب الاسم:
properties.Remove("Year");

Assert.AreEqual(2, properties.Count);

// 3 - مسح المجموعة بأكملها مرة واحدة:
properties.Clear();

Assert.AreEqual(0, properties.Count);
```

### أنظر أيضا

* class [CustomXmlProperty](../../customxmlproperty/)
* class [CustomXmlPropertyCollection](../)
* مساحة الاسم [Aspose.Words.Markup](../../../aspose.words.markup/)
* المجسم [Aspose.Words](../../../)
