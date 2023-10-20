---
title: Font.UnderlineColor
linktitle: UnderlineColor
articleTitle: UnderlineColor
second_title: Aspose.Words لـ .NET
description: Font UnderlineColor ملكية. الحصول على أو تعيين لون التسطير المطبق على الخط في C#.
type: docs
weight: 540
url: /ar/net/aspose.words/font/underlinecolor/
---
## Font.UnderlineColor property

الحصول على أو تعيين لون التسطير المطبق على الخط.

```csharp
public Color UnderlineColor { get; set; }
```

## أمثلة

يوضح كيفية تكوين نمط ولون التسطير في النص.

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
