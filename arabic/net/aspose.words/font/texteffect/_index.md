---
title: Font.TextEffect
linktitle: TextEffect
articleTitle: TextEffect
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font TextEffect لتخصيص رسوم متحركة للخطوط بسهولة، وتعزيز تصميماتك بتأثيرات نصية ديناميكية للحصول على تجربة مستخدم جذابة.
type: docs
weight: 460
url: /ar/net/aspose.words/font/texteffect/
---
## Font.TextEffect property

يحصل على تأثير الرسوم المتحركة للخط أو يعينه.

```csharp
public TextEffect TextEffect { get; set; }
```

## أمثلة

يوضح كيفية تطبيق تأثير مرئي على الجري.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 36;
builder.Font.TextEffect = TextEffect.SparkleText;

builder.Writeln("Text with a sparkle effect.");

// تدعم الإصدارات الأقدم من Microsoft Word تأثيرات الرسوم المتحركة للخطوط فقط.
doc.Save(ArtifactsDir + "Font.SparklingText.doc");
```

### أنظر أيضا

* enum [TextEffect](../../texteffect/)
* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
