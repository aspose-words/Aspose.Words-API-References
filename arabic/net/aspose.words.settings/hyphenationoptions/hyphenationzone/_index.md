---
title: HyphenationOptions.HyphenationZone
second_title: Aspose.Words لمراجع .NET API
description: HyphenationOptions ملكية. الحصول على أو تعيين المسافة بـ 1/20 نقطة من الهامش الأيمن الذي لا تريد وصل الكلمات فيه. القيمة الافتراضية لهذه الخاصية هي 360 0.25 بوصة.
type: docs
weight: 50
url: /ar/net/aspose.words.settings/hyphenationoptions/hyphenationzone/
---
## HyphenationOptions.HyphenationZone property

الحصول على أو تعيين المسافة بـ 1/20 نقطة من الهامش الأيمن الذي لا تريد وصل الكلمات فيه. القيمة الافتراضية لهذه الخاصية هي 360 (0.25 بوصة).

```csharp
public int HyphenationZone { get; set; }
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

* class [HyphenationOptions](../)
* مساحة الاسم [Aspose.Words.Settings](../../hyphenationoptions/)
* المجسم [Aspose.Words](../../../)


