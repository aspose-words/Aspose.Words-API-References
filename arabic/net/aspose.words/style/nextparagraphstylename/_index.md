---
title: Style.NextParagraphStyleName
linktitle: NextParagraphStyleName
articleTitle: NextParagraphStyleName
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية استخدام خاصية NextParagraphStyleName بشكل فعال لأتمتة تطبيق الأسلوب للفقرات الجديدة، مما يعزز تنسيق مستندك.
type: docs
weight: 140
url: /ar/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

يحصل على/يحدد اسم النمط الذي سيتم تطبيقه تلقائيًا على فقرة جديدة مدرجة بعد فقرة a بتنسيق النمط المحدد.

```csharp
public string NextParagraphStyleName { get; set; }
```

## ملاحظات

لا يستخدم Aspose.Words هذه الخاصية. سيتم تطبيق نمط الفقرة التالية تلقائيًا فقط عند تحرير المستند في MS Word.

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
