---
title: ParagraphFormat.MirrorIndents
linktitle: MirrorIndents
articleTitle: MirrorIndents
second_title: Aspose.Words لـ .NET
description: اكتشف كيف تعمل خاصية ParagraphFormat MirrorIndents على تحسين تنسيق مستندك من خلال ضمان وجود مسافة بادئة متسقة بين السطور اليمنى واليسرى للحصول على مظهر أنيق.
type: docs
weight: 240
url: /ar/net/aspose.words/paragraphformat/mirrorindents/
---
## ParagraphFormat.MirrorIndents property

يحصل على علم أو يعينه للإشارة إلى ما إذا كانت المسافات البادئة اليسرى واليمنى بنفس العرض.

```csharp
public bool MirrorIndents { get; set; }
```

## أمثلة

إظهار كيفية جعل المسافات البادئة اليمنى واليسرى متماثلة.

```csharp
Document doc = new Document(MyDir + "Document.docx");
ParagraphFormat format = doc.FirstSection.Body.Paragraphs[0].ParagraphFormat;

format.MirrorIndents = true;

doc.Save(ArtifactsDir + "ParagraphFormat.MirrorIndents.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
