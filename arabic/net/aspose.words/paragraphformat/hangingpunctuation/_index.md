---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: Aspose.Words لـ .NET
description: ParagraphFormat HangingPunctuation ملكية. الحصول على علامة تشير إلى ما إذا كانت علامات الترقيم المعلقة ممكّنة للفقرة الحالية أو تعيينها في C#.
type: docs
weight: 130
url: /ar/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

الحصول على علامة تشير إلى ما إذا كانت علامات الترقيم المعلقة ممكّنة للفقرة الحالية أو تعيينها.

```csharp
public bool HangingPunctuation { get; set; }
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
