---
title: GetEnumerator
second_title: Aspose.Words لمراجع .NET API
description: الحصول على كائن العداد الذي يقوم بتعداد الأنماط بالترتيب الأبجدي لأسمائها.
type: docs
weight: 90
url: /ar/net/aspose.words/stylecollection/getenumerator/
---
## StyleCollection.GetEnumerator method

الحصول على كائن العداد الذي يقوم بتعداد الأنماط بالترتيب الأبجدي لأسمائها.

```csharp
public IEnumerator<Style> GetEnumerator()
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

* class [Style](../../style)
* class [StyleCollection](../../stylecollection)
* مساحة الاسم [Aspose.Words](../../stylecollection)
* المجسم [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->