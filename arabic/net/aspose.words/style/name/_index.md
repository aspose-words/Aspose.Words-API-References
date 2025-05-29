---
title: Style.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية اسم النمط، وقم بإدارة أنماطك وتخصيصها بسهولة لتحسين مرونة التصميم وتجربة المستخدم.
type: docs
weight: 130
url: /ar/net/aspose.words/style/name/
---
## Style.Name property

يحصل على اسم النمط أو يعينه.

```csharp
public string Name { get; set; }
```

## ملاحظات

لا يمكن أن تكون سلسلة فارغة.

إذا كان هناك نمط بهذا الاسم في المجموعة، فسيحل هذا النمط محله. ستُشير جميع العقد المتأثرة إلى النمط الجديد.

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

يوضح كيفية استنساخ نمط المستند.

```csharp
Document doc = new Document();

// تقوم طريقة AddCopy بإنشاء نسخة من النمط المحدد و
// يتم إنشاء اسم جديد للنمط تلقائيًا، مثل "Heading 1_0".
Style newStyle = doc.Styles.AddCopy(doc.Styles["Heading 1"]);

//استخدم خاصية "الاسم" الخاصة بالنمط لتغيير الاسم الذي يميز النمط.
newStyle.Name = "My Heading 1";

// تحتوي مستندنا الآن على نمطين متطابقين في المظهر ولكن بأسماء مختلفة.
// تغيير إعدادات أحد الأنماط لا يؤثر على الآخر.
newStyle.Font.Color = Color.Red;

Assert.AreEqual("My Heading 1", newStyle.Name);
Assert.AreEqual("Heading 1", doc.Styles["Heading 1"].Name);

Assert.AreEqual(doc.Styles["Heading 1"].Type, newStyle.Type);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Name, newStyle.Font.Name);
Assert.AreEqual(doc.Styles["Heading 1"].Font.Size, newStyle.Font.Size);
Assert.AreNotEqual(doc.Styles["Heading 1"].Font.Color, newStyle.Font.Color);
```

### أنظر أيضا

* class [Style](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
