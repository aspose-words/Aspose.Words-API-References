---
title: Style.Type
second_title: Aspose.Words لمراجع .NET API
description: Style ملكية. الحصول على نوع النمط فقرة أو حرف.
type: docs
weight: 180
url: /ar/net/aspose.words/style/type/
---
## Style.Type property

الحصول على نوع النمط (فقرة أو حرف).

```csharp
public StyleType Type { get; }
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

* enum [StyleType](../../styletype/)
* class [Style](../)
* مساحة الاسم [Aspose.Words](../../style/)
* المجسم [Aspose.Words](../../../)


