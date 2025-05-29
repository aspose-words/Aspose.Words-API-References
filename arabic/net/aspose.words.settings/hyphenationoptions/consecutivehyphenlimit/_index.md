---
title: HyphenationOptions.ConsecutiveHyphenLimit
linktitle: ConsecutiveHyphenLimit
articleTitle: ConsecutiveHyphenLimit
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ConsecutiveHyphenLimit في HyphenationOptions. تحكّم في استخدام الواصلات في نصك لتحسين سهولة القراءة والتنسيق. القيمة الافتراضية: 0.
type: docs
weight: 30
url: /ar/net/aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/
---
## HyphenationOptions.ConsecutiveHyphenLimit property

يحصل على أو يعين الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بواصلات. القيمة الافتراضية لهذه الخاصية هي 0.

```csharp
public int ConsecutiveHyphenLimit { get; set; }
```

## ملاحظات

إذا تم تعيين قيمة هذه الخاصية على 0، فيمكن أن ينتهي أي عدد من الأسطر المتتالية بواصلات.

لا يكون للخاصية أي تأثير عند الحفظ بتنسيقات الصفحات الثابتة مثل PDF.

## أمثلة

يوضح كيفية تكوين الوصلة التلقائية.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Size = 24;
builder.Writeln("Lorem ipsum dolor sit amet, consectetur adipiscing elit, " +
                "sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

doc.HyphenationOptions.AutoHyphenation = true;
doc.HyphenationOptions.ConsecutiveHyphenLimit = 2;
doc.HyphenationOptions.HyphenationZone = 720;
doc.HyphenationOptions.HyphenateCaps = true;

doc.Save(ArtifactsDir + "Document.HyphenationOptions.docx");
```

### أنظر أيضا

* class [HyphenationOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../../aspose.words.settings/)
* المجسم [Aspose.Words](../../../)
