---
title: PageSetup.TextOrientation
linktitle: TextOrientation
articleTitle: TextOrientation
second_title: Aspose.Words لـ .NET
description: PageSetup TextOrientation ملكية. يسمح بالتحديدTextOrientation للصفحة بأكملها. القيمة الافتراضية هيHorizontal في C#.
type: docs
weight: 430
url: /ar/net/aspose.words/pagesetup/textorientation/
---
## PageSetup.TextOrientation property

يسمح بالتحديد`TextOrientation` للصفحة بأكملها. القيمة الافتراضية هيHorizontal

```csharp
public TextOrientation TextOrientation { get; set; }
```

## ملاحظات

هذه الخاصية مدعومة فقط لتنسيقات MS Word الأصلية DOCX وWML وRTF وDOC.

## أمثلة

يوضح كيفية ضبط اتجاه النص.

```csharp
Document doc = new Document();

DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// اضبط خاصية "TextOrientation" على "TextOrientation.Upward" لتدوير النص بالكامل بمقدار 90 درجة
// إلى اليمين بحيث ينتقل كل النص من اليسار إلى اليمين من أعلى إلى أسفل.
PageSetup pageSetup = doc.Sections[0].PageSetup;
pageSetup.TextOrientation = TextOrientation.Upward;

doc.Save(ArtifactsDir + "PageSetup.SetTextOrientation.docx");
```

### أنظر أيضا

* enum [TextOrientation](../../textorientation/)
* class [PageSetup](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
