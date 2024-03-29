---
title: ViewOptions.DisplayBackgroundShape
linktitle: DisplayBackgroundShape
articleTitle: DisplayBackgroundShape
second_title: Aspose.Words لـ .NET
description: ViewOptions DisplayBackgroundShape ملكية. يتحكم في عرض شكل الخلفية في عرض تخطيط الطباعة في C#.
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

// مصدر المستند له خلفية ملونة مسطحة،
// الذي سيؤدي وجوده إلى تعيين علامة "DisplayBackgroundShape" على "صحيح".
Assert.True(doc.ViewOptions.DisplayBackgroundShape);

// احتفظ بـ "DisplayBackgroundShape" على أنه "صحيح" حتى يعرض المستند لون الخلفية.
// قد يؤثر هذا على بعض ألوان النص لتحسين الرؤية.
// اضبط "DisplayBackgroundShape" على "خطأ" حتى لا يتم عرض لون الخلفية.
doc.ViewOptions.DisplayBackgroundShape = displayBackgroundShape;

doc.Save(ArtifactsDir + "ViewOptions.DisplayBackgroundShape.docx");
```

### أنظر أيضا

* class [ViewOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
