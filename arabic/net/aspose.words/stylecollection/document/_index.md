---
title: StyleCollection.Document
linktitle: Document
articleTitle: Document
second_title: Aspose.Words لـ .NET
description: تمتع بالوصول إلى مستند المالك بسهولة مع StyleCollection. اكتشف إدارة مستندات سلسة وحسّن سير عملك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words/stylecollection/document/
---
## StyleCollection.Document property

يحصل على مستند المالك.

```csharp
public DocumentBase Document { get; }
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

* class [DocumentBase](../../documentbase/)
* class [StyleCollection](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
