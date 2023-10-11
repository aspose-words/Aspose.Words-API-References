---
title: Font.HighlightColor
second_title: Aspose.Words لمراجع .NET API
description: Font ملكية. الحصول على أو تعيين لون التمييز علامة التحديد.
type: docs
weight: 150
url: /ar/net/aspose.words/font/highlightcolor/
---
## Font.HighlightColor property

الحصول على أو تعيين لون التمييز (علامة التحديد).

```csharp
public Color HighlightColor { get; set; }
```

### أمثلة

يوضح كيفية تنسيق مجموعة من النص باستخدام خاصية الخط الخاصة به.

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
* مساحة الاسم [Aspose.Words](../../font/)
* المجسم [Aspose.Words](../../../)


