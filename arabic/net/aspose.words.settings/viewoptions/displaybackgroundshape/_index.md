---
title: ViewOptions.DisplayBackgroundShape
linktitle: DisplayBackgroundShape
articleTitle: DisplayBackgroundShape
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية DisplayBackgroundShape في ViewOptions لتحسين تخطيط الطباعة الخاص بك باستخدام أشكال خلفية قابلة للتخصيص للحصول على مظهر أنيق.
type: docs
weight: 10
url: /ar/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

يتحكم في عرض شكل الخلفية في عرض تخطيط الطباعة.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

## أمثلة

يوضح كيفية إخفاء/عرض صور خلفية المستند في خيارات العرض.

```csharp
// استخدم سلسلة HTML لإنشاء مستند جديد بلون خلفية مسطح.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// المصدر للمستند له خلفية ملونة مسطحة،
// سيؤدي وجودها إلى تعيين علم "DisplayBackgroundShape" إلى "true".
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

//احتفظ بـ "DisplayBackgroundShape" على القيمة "true" لجعل المستند يعرض لون الخلفية.
// قد يؤثر هذا على بعض ألوان النص لتحسين الرؤية.
// قم بضبط "DisplayBackgroundShape" على "false" لعدم عرض لون الخلفية.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### أنظر أيضا

* class [ViewOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
