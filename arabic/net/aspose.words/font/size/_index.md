---
title: Font.Size
linktitle: Size
articleTitle: Size
second_title: Aspose.Words لـ .NET
description: اضبط حجم الخط بسهولة باستخدام خاصية "حجم الخط". خصّص نصك بالنقاط لتحسين سهولة القراءة وجاذبية التصميم.
type: docs
weight: 350
url: /ar/net/aspose.words/font/size/
---
## Font.Size property

يحصل على حجم الخط بالنقاط أو يعينه.

```csharp
public double Size { get; set; }
```

## أمثلة

يوضح كيفية تنسيق سلسلة من النص باستخدام خاصية الخط الخاصة به.

```csharp
Document doc = new Document();
Run run = new Run(doc, "Hello world!");

Aspose.Words.Font font = run.Font;
font.Name = "Courier New";
font.Size = 36;
font.HighlightColor = Color.Yellow;

doc.FirstSection.Body.FirstParagraph.AppendChild(run);
doc.Save(ArtifactsDir + "Font.CreateFormattedRun.docx");
```

يوضح كيفية إدراج نص منسق باستخدام DocumentBuilder.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// حدد تنسيق الخط، ثم أضف النص.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### أنظر أيضا

* class [Font](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
