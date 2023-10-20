---
title: ParagraphFormat.LeftIndent
linktitle: LeftIndent
articleTitle: LeftIndent
second_title: Aspose.Words لـ .NET
description: ParagraphFormat LeftIndent ملكية. الحصول على أو تعيين القيمة بالنقاط التي تمثل المسافة البادئة اليسرى للفقرة في C#.
type: docs
weight: 180
url: /ar/net/aspose.words/paragraphformat/leftindent/
---
## ParagraphFormat.LeftIndent property

الحصول على أو تعيين القيمة (بالنقاط) التي تمثل المسافة البادئة اليسرى للفقرة.

```csharp
public double LeftIndent { get; set; }
```

## أمثلة

يوضح كيفية تكوين تنسيق الفقرة لإنشاء نص خارج المركز.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// توسيط كل النص الذي يكتبه منشئ المستندات، وإعداد المسافات البادئة.
// سيؤدي تكوين المسافة البادئة أدناه إلى إنشاء نص يتم وضعه بشكل غير متماثل على الصفحة.
// "المركز" الذي نقوم بمحاذاة النص إليه سيكون منتصف نص النص، وليس منتصف الصفحة.
ParagraphFormat paragraphFormat = builder.ParagraphFormat;
paragraphFormat.Alignment = ParagraphAlignment.Center;
paragraphFormat.LeftIndent = 100;
paragraphFormat.RightIndent = 50;
paragraphFormat.SpaceAfter = 25;

builder.Writeln(
    "This paragraph demonstrates how left and right indentation affects word wrapping.");
builder.Writeln(
    "The space between the above paragraph and this one depends on the DocumentBuilder's paragraph format.");

doc.Save(ArtifactsDir + "DocumentBuilder.SetParagraphFormatting.docx");
```

### أنظر أيضا

* class [ParagraphFormat](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
