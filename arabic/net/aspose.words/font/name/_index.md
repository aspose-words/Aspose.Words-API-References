---
title: Font.Name
linktitle: Name
articleTitle: Name
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية اسم الخط لتخصيص أنماط الخطوط الخاصة بك وتعيينها بسهولة، مما يعزز جاذبية تصميمك وقابليته للقراءة.
type: docs
weight: 230
url: /ar/net/aspose.words/font/name/
---
## Font.Name property

يحصل على اسم الخط أو يعينه.

```csharp
public string Name { get; set; }
```

## ملاحظات

عند الحصول عليها، يعود[`NameAscii`](../nameascii/).

عند الضبط، يتم ضبط[`NameAscii`](../nameascii/) ،[`NameBi`](../namebi/) ،[`NameFarEast`](../namefareast/) و[`NameOther`](../nameother/) إلى القيمة المحددة.

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
