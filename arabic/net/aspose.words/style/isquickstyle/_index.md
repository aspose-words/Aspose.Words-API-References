---
title: Style.IsQuickStyle
linktitle: IsQuickStyle
articleTitle: IsQuickStyle
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية IsQuickStyle على تعزيز تجربة MS Word الخاصة بك من خلال عرض الأنماط في معرض الأنماط السريعة لسهولة الوصول وتحسين سير العمل.
type: docs
weight: 80
url: /ar/net/aspose.words/style/isquickstyle/
---
## Style.IsQuickStyle property

يحدد ما إذا كان سيتم عرض هذا النمط في معرض الأنماط السريعة داخل واجهة مستخدم MS Word.

```csharp
public bool IsQuickStyle { get; set; }
```

## أمثلة

يوضح كيفية الوصول إلى مجموعة أنماط المستند.

```csharp
Document doc = new Document();

Assert.AreEqual(4, doc.Styles.Count);

// قم بإحصاء وإدراج جميع الأنماط التي يحتويها المستند الذي تم إنشاؤه باستخدام Aspose.Words بشكل افتراضي.
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

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
