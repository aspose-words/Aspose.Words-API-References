---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words لـ .NET
description: اكتشف ميزة Font NoProofing. امنع التدقيق الإملائي للنصوص المنسقة لتصاميم أكثر دقة. حسّن مستنداتك بدقة واحترافية!
type: docs
weight: 280
url: /ar/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

صحيح عندما لا يتم التحقق من صحة الأحرف المنسقة.

```csharp
public bool NoProofing { get; set; }
```

## أمثلة

يوضح كيفية منع التدقيق الإملائي للنص بواسطة Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// عادةً ما يسلط Microsoft Word الضوء على الأخطاء الإملائية من خلال وضع خط أحمر متعرج أسفلها.
// يمكننا إلغاء تعيين علامة "NoProofing" لإنشاء جزء من النص
// يتجاوز مدقق الإملاء مع تعطيله تمامًا.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
