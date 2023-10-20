---
title: Font.NoProofing
linktitle: NoProofing
articleTitle: NoProofing
second_title: Aspose.Words لـ .NET
description: Font NoProofing ملكية. صحيح عندما لا يتم التدقيق الإملائي على الأحرف المنسقة في C#.
type: docs
weight: 280
url: /ar/net/aspose.words/font/noproofing/
---
## Font.NoProofing property

صحيح عندما لا يتم التدقيق الإملائي على الأحرف المنسقة.

```csharp
public bool NoProofing { get; set; }
```

## أمثلة

يوضح كيفية منع النص من التدقيق الإملائي بواسطة Microsoft Word.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// عادةً، يركز برنامج Microsoft Word على الأخطاء الإملائية من خلال تسطير أحمر متعرج.
// يمكننا إلغاء تعيين علامة "NoProofing" لإنشاء جزء من النص
// يتجاوز المدقق الإملائي أثناء تعطيله تمامًا.
builder.Font.NoProofing = true;

builder.Writeln("Proofing has been disabled, so these spelking errrs will not display red lines underneath.");

doc.Save(ArtifactsDir + "Font.NoProofing.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
