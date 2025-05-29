---
title: HyphenationOptions.AutoHyphenation
linktitle: AutoHyphenation
articleTitle: AutoHyphenation
second_title: Aspose.Words لـ .NET
description: تحكم في وضع الواصلة تلقائيًا باستخدام خاصية HyphenationOptions. حسّن سهولة قراءة مستندك بسهولة عن طريق تفعيل هذه الميزة أو إيقافها.
type: docs
weight: 20
url: /ar/net/aspose.words.settings/hyphenationoptions/autohyphenation/
---
## HyphenationOptions.AutoHyphenation property

يحصل على القيمة أو يعينها لتحديد ما إذا كان يتم تشغيل الوصل التلقائي للمستند. القيمة الافتراضية لهذه الخاصية هي`خطأ شنيع` .

```csharp
public bool AutoHyphenation { get; set; }
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
