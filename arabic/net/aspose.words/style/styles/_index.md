---
title: Style.Styles
second_title: Aspose.Words لمراجع .NET API
description: Style ملكية. الحصول على مجموعة الأنماط التي ينتمي إليها هذا النمط.
type: docs
weight: 170
url: /ar/net/aspose.words/style/styles/
---
## Style.Styles property

الحصول على مجموعة الأنماط التي ينتمي إليها هذا النمط.

```csharp
public StyleCollection Styles { get; }
```

### أمثلة

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// تعداد وسرد جميع الأنماط التي يحتوي عليها المستند الذي تم إنشاؤه باستخدام Aspose.Words بشكل افتراضي.
using (IEnumerator<Style> stylesEnum = doc.Styles.GetEnumerator())
{
    while (stylesEnum.MoveNext())
    {
        Style curStyle = stylesEnum.Current;
        Console.WriteLine($"Style name:\t\"{curStyle.Name}\", of type \"{curStyle.Type}\"");
        Console.WriteLine($"\tSubsequent style:\t{curStyle.NextParagraphStyleName}");
        Console.WriteLine($"\tIs heading:\t\t\t{curStyle.IsHeading}");
        Console.WriteLine($"\tIs QuickStyle:\t\t{curStyle.IsQuickStyle}");

        Assert.AreEqual(doc, curStyle.Document);
    }
}
```

### أنظر أيضا

* class [StyleCollection](../../stylecollection/)
* class [Style](../)
* مساحة الاسم [Aspose.Words](../../style/)
* المجسم [Aspose.Words](../../../)


