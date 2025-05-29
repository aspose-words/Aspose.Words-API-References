---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية PageSetup TextOrientation لضبط اتجاه نص الصفحة بسهولة. خصّص تخطيطك بخيارات تتجاوز الوضع الأفقي الافتراضي.
type: docs
weight: 430
url: /ar/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

يسمح بتحديد`TextOrientation` للصفحة بأكملها. القيمة الافتراضية هيHorizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## ملاحظات

يتم دعم هذه الخاصية فقط لتنسيقات MS Word الأصلية DOCX وWML وRTF وDOC.

## أمثلة

يوضح كيفية ضبط اتجاه النص.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// اضبط خاصية "TextOrientation" على "TextOrientation.Upward" لتدوير النص بالكامل بزاوية 90 درجة
// إلى اليمين بحيث ينتقل النص بأكمله من اليسار إلى اليمين من أعلى إلى أسفل.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### أنظر أيضا

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
