---
title: Style.NextParagraphStyleName
linktitle: NextParagraphStyleName
articleTitle: NextParagraphStyleName
second_title: Aspose.Words لـ .NET
description: Style NextParagraphStyleName ملكية. الحصول على/تعيين اسم النمط الذي سيتم تطبيقه تلقائيًا على فقرة جديدة تم إدراجها بعد a فقرة منسقة بالنمط المحدد في C#.
type: docs
weight: 130
url: /ar/net/aspose.words/style/nextparagraphstylename/
---
## Style.NextParagraphStyleName property

الحصول على/تعيين اسم النمط الذي سيتم تطبيقه تلقائيًا على فقرة جديدة تم إدراجها بعد a فقرة منسقة بالنمط المحدد.

```csharp
public string NextParagraphStyleName { get; set; }
```

## ملاحظات

لا يتم استخدام هذه الخاصية بواسطة Aspose.Words. سيتم تطبيق نمط الفقرة التالي فقط تلقائيًا عند تحرير المستند في برنامج MS Word.

## أمثلة

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

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
