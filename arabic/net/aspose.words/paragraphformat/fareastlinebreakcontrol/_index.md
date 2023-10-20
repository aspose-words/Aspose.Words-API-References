---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words لـ .NET
description: ParagraphFormat FarEastLineBreakControl ملكية. الحصول على علامة تشير إلى ما إذا كانت قواعد فصل الأسطر في شرق آسيا مطبقة على الفقرة الحالية أو تعيينها في C#.
type: docs
weight: 110
url: /ar/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

الحصول على علامة تشير إلى ما إذا كانت قواعد فصل الأسطر في شرق آسيا مطبقة على الفقرة الحالية أو تعيينها.

```csharp
public bool FarEastLineBreakControl { get; set; }
```

## أمثلة

يوضح كيفية تعيين خصائص خاصة للطباعة الآسيوية.

```csharp
Document doc = new Document(MyDir + "Document.docx");

ParagraphFormat format = doc.FirstSection.Body.FirstParagraph.ParagraphFormat;
format.FarEastLineBreakControl = true;
format.WordWrap = false;
format.HangingPunctuation = true;

doc.Save(ArtifactsDir + "ParagraphFormat.AsianTypographyProperties.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
