---
title: HyphenationOptions.HyphenateCaps
linktitle: HyphenateCaps
articleTitle: HyphenateCaps
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية HyphenateCaps في HyphenationOptions. تحكّم بسهولة في وضع الواصلة للكلمات المكتوبة بأحرف كبيرة - الإعداد الافتراضي هو true. حسّن نصك اليوم!
type: docs
weight: 40
url: /ar/net/aspose.words.settings/hyphenationoptions/hyphenatecaps/
---
## HyphenationOptions.HyphenateCaps property

يحصل على القيمة أو يعينها لتحديد ما إذا كانت الكلمات المكتوبة بأحرف كبيرة جميعها موصولة بواصلة. القيمة الافتراضية لهذه الخاصية هي`حقيقي` .

```csharp
public bool HyphenateCaps { get; set; }
```

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
