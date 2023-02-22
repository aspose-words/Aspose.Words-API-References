---
title: Style.NextParagraphStyleName
second_title: Aspose.Words لمراجع .NET API
description: Style ملكية. يحصل / يحدد اسم النمط ليتم تطبيقه تلقائيًا على فقرة جديدة مدرجة بعد a فقرة منسقة بالنمط المحدد.
type: docs
weight: 120
url: /ar/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

يحصل / يحدد اسم النمط ليتم تطبيقه تلقائيًا على فقرة جديدة مدرجة بعد a فقرة منسقة بالنمط المحدد.

```csharp
public string NextParagraphStyleName { get; set; }
```

### ملاحظات

لا تستخدم Aspose.Words هذه الخاصية. سيتم تطبيق نمط الفقرة التالي فقط تلقائيًا عندما تقوم بتحرير المستند في MS Word.

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

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../style/)
* المجسم [Aspose.Words](../../../)


