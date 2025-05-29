---
title: ParagraphFormat.FarEastLineBreakControl
linktitle: FarEastLineBreakControl
articleTitle: FarEastLineBreakControl
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ParagraphFormat FarEastLineBreakControl، التي تعمل على تمكين قواعد كسر الأسطر في شرق آسيا للحصول على تنسيق نص دقيق في مستنداتك.
type: docs
weight: 110
url: /ar/net/aspose.words/paragraphformat/fareastlinebreakcontrol/
---
## ParagraphFormat.FarEastLineBreakControl property

يحصل على علم أو يعينه للإشارة إلى ما إذا كانت قواعد كسر الأسطر في شرق آسيا مطبقة على الفقرة الحالية.

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
