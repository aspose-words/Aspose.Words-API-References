---
title: Font.TextEffect
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على تأثير الخط المتحرك أو تعيينه.
type: docs
weight: 450
url: /ar/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

الحصول على تأثير الخط المتحرك أو تعيينه.

```csharp
public TextEffect TextEffect { get; set; }
```

### أمثلة

يوضح كيفية تطبيق تأثير مرئي على الجري.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// الإصدارات الأقدم من Microsoft Word تدعم فقط تأثيرات الرسوم المتحركة للخطوط.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### أنظر أيضا

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


