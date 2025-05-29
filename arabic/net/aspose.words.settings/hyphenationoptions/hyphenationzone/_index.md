---
title: HyphenationOptions.HyphenationZone
linktitle: HyphenationZone
articleTitle: HyphenationZone
second_title: Aspose.Words لـ .NET
description: حسّن تخطيط النص باستخدام خاصية HyphenationZone. تحكّم في مسافة الواصلة من الهامش الأيمن لمستندات أكثر دقةً واحترافية.
type: docs
weight: 50
url: /ar/net/aspose.words.settings/hyphenationoptions/hyphenationzone/
---
## HyphenationOptions.HyphenationZone property

يحصل على أو يضبط المسافة بمقدار 1/20 من نقطة من الهامش الأيمن الذي لا تريد أن تقوم بوضع علامة وصل بين الكلمات فيه. القيمة الافتراضية لهذه الخاصية هي 360 (0.25 بوصة).

```csharp
public int HyphenationZone { get; set; }
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
