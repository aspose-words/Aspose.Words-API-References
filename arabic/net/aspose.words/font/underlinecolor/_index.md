---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Font UnderlineColor لتخصيص لون خطك بسهولة لتحسين تصميم النص وتحسين المظهر المرئي.
type: docs
weight: 550
url: /ar/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

يحصل على لون الخط السفلي المطبق على الخط أو يعينه.

```csharp
public Color UnderlineColor { get; set; }
```

## أمثلة

يوضح كيفية تكوين نمط ولون تسطير النص.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Underline = Underline.Dotted;
builder.Font.UnderlineColor = Color.Red;

builder.Writeln("Underlined text.");

doc.Save(ArtifactsDir + "Font.Underlines.docx");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
