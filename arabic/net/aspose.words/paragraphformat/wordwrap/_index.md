---
title: ParagraphFormat.WordWrap
linktitle: WordWrap
articleTitle: WordWrap
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تؤثر خاصية ParagraphFormat WordWrap على التفاف النص في Word. تعلم كيفية التحكم في تدفق النص اللاتيني لتحسين قابلية قراءة المستند.
type: docs
weight: 420
url: /ar/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

إذا كانت هذه الخاصية`خطأ شنيع` يمكن تغليف النص اللاتيني في منتصف الكلمة بالكلمات الكاملة.

```csharp
public bool WordWrap { get; set; }
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
