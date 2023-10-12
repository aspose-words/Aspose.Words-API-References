---
title: HyphenationOptions.ConsecutiveHyphenLimit
second_title: Aspose.Words لمراجع .NET API
description: HyphenationOptions ملكية. الحصول على أو تعيين الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بواصلات. القيمة الافتراضية لهذه الخاصية هي 0.
type: docs
weight: 30
url: /ar/net/aspose.words.settings/hyphenationoptions/consecutivehyphenlimit/
---
## HyphenationOptions.ConsecutiveHyphenLimit property

الحصول على أو تعيين الحد الأقصى لعدد الأسطر المتتالية التي يمكن أن تنتهي بواصلات. القيمة الافتراضية لهذه الخاصية هي 0.

```csharp
public int ConsecutiveHyphenLimit { get; set; }
```

### ملاحظات

إذا تم تعيين قيمة هذه الخاصية على 0، فإن أي عدد من الأسطر المتتالية يمكن أن ينتهي بواصلات.

لا يكون لهذه الخاصية أي تأثير عند الحفظ في تنسيقات الصفحات الثابتة، مثل PDF.

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

* class [HyphenationOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../hyphenationoptions/)
* المجسم [Aspose.Words](../../../)


