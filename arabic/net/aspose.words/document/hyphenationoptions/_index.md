---
title: Document.HyphenationOptions
linktitle: HyphenationOptions
articleTitle: HyphenationOptions
second_title: Aspose.Words لـ .NET
description: استكشف خاصية Document HyphenationOptions لتخصيص إعدادات الوصل، مما يعزز قابلية القراءة ويحسن عرض المستند.
type: docs
weight: 220
url: /ar/net/aspose.words/document/hyphenationoptions/
---
## Document.HyphenationOptions property

يوفر الوصول إلى خيارات وضع علامات الوصل في المستند.

```csharp
public HyphenationOptions HyphenationOptions { get; }
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

* class [HyphenationOptions](../../../aspose.words.settings/hyphenationoptions/)
* class [Document](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
