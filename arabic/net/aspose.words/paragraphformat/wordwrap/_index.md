---
title: ParagraphFormat.WordWrap
second_title: Aspose.Words لمراجع .NET API
description: ParagraphFormat ملكية. إذا كانت هذه الخاصيةخطأ شنيع  يمكن تغليف النص اللاتيني الموجود في منتصف الكلمة بـ الفقرة الحالية. وإلا فسيتم تغليف النص اللاتيني بكلمات كاملة.
type: docs
weight: 410
url: /ar/net/aspose.words/paragraphformat/wordwrap/
---
## ParagraphFormat.WordWrap property

إذا كانت هذه الخاصية`خطأ شنيع` ، يمكن تغليف النص اللاتيني الموجود في منتصف الكلمة بـ الفقرة الحالية. وإلا فسيتم تغليف النص اللاتيني بكلمات كاملة.

```csharp
public bool WordWrap { get; set; }
```

### أمثلة

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
* مساحة الاسم [Aspose.Words](../../paragraphformat/)
* المجسم [Aspose.Words](../../../)


