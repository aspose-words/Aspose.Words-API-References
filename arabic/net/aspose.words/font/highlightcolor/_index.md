---
title: Font.HighlightColor
linktitle: HighlightColor
articleTitle: HighlightColor
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية "لون تمييز الخط" - خصص لون تمييز نصك بسهولة لتحسين قابلية القراءة وجاذبيته البصرية. ارتقِ بتصميمك!
type: docs
weight: 150
url: /ar/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

يحصل على لون التمييز (العلامة) أو يعينه.

```csharp
public Color HighlightColor { get; set; }
```

## أمثلة

يوضح كيفية تنسيق سلسلة من النص باستخدام خاصية الخط الخاصة به.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
