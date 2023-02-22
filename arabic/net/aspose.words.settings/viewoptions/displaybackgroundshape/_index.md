---
title: ViewOptions.DisplayBackgroundShape
second_title: Aspose.Words لمراجع .NET API
description: ViewOptions ملكية. يتحكم في عرض شكل الخلفية في عرض تخطيط الطباعة.
type: docs
weight: 10
url: /ar/net/aspose.words.settings/viewoptions/displaybackgroundshape/
---
## ViewOptions.DisplayBackgroundShape property

يتحكم في عرض شكل الخلفية في عرض تخطيط الطباعة.

```csharp
public bool DisplayBackgroundShape { get; set; }
```

### أمثلة

يوضح كيفية إخفاء / عرض صور خلفية المستند في خيارات العرض.

```csharp
// استخدم سلسلة HTML لإنشاء مستند جديد بلون خلفية مسطح.
const string html = 
@"<html>
    <body style='background-color: blue'>
        <p>Hello world!</p>
    </body>
</html>";

Document doc = new Document(new MemoryStream(Encoding.Unicode.GetBytes(html)));

// يحتوي مصدر المستند على خلفية ملونة مسطحة ،
// سيؤدي وجودها إلى تعيين علامة "DisplayBackgroundShape" على "true".
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// احتفظ بـ "DisplayBackgroundShape" على أنها "true" لجعل المستند يعرض لون الخلفية.
// قد يؤثر هذا على بعض ألوان النص لتحسين الرؤية.
// اضبط "DisplayBackgroundShape" على "false" لعدم عرض لون الخلفية.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### أنظر أيضا

* class [ViewOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../viewoptions/)
* المجسم [Aspose.Words](../../../)


