---
title: ParagraphFormat.HangingPunctuation
linktitle: HangingPunctuation
articleTitle: HangingPunctuation
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تحسين تصميم نصك باستخدام خاصية علامات الترقيم المعلقة في ParagraphFormat. حسّن سهولة القراءة والأسلوب بسهولة!
type: docs
weight: 130
url: /ar/net/aspose.words/paragraphformat/hangingpunctuation/
---
## ParagraphFormat.HangingPunctuation property

يحصل على علم أو يعينه للإشارة إلى ما إذا كان تم تمكين علامات الترقيم المعلقة للفقرة الحالية.

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
