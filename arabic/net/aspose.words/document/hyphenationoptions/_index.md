---
title: Document.HyphenationOptions
second_title: Aspose.Words لمراجع .NET API
description: Document ملكية. يوفر الوصول إلى خيارات الواصلة في المستند.
type: docs
weight: 210
url: /ar/net/aspose.words/document/hyphenationoptions/
---
## Document.HyphenationOptions property

يوفر الوصول إلى خيارات الواصلة في المستند.

```csharp
public HyphenationOptions HyphenationOptions { get; }
```

### أمثلة

يوضح كيفية تكوين الواصلة التلقائية.

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
* مساحة الاسم [Aspose.Words](../../document/)
* المجسم [Aspose.Words](../../../)


