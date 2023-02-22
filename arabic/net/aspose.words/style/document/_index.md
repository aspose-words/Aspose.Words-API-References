---
title: Style.Document
second_title: Aspose.Words لمراجع .NET API
description: Style ملكية. الحصول على مستند المالك.
type: docs
weight: 40
url: /ar/net/aspose.words/style/document/
---
## Style.Document property

الحصول على مستند المالك.

```csharp
public DocumentBase Document { get; }
```

### أمثلة

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// تعداد وإدراج جميع الأنماط التي تم إنشاؤها باستخدام Aspose.Words تحتوي على كل الأنماط التي تم إنشاؤها باستخدام Aspose.Words بشكل افتراضي.
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

* class [DocumentBase](../../documentbase/)
* class [Style](../)
* مساحة الاسم [Aspose.Words](../../style/)
* المجسم [Aspose.Words](../../../)


