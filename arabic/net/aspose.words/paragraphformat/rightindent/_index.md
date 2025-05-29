---
title: ParagraphFormat.RightIndent
linktitle: RightIndent
articleTitle: RightIndent
second_title: Aspose.Words لـ .NET
description: اكتشف كيفية تعديل المسافة البادئة اليمنى لفقراتك بسهولة باستخدام خاصية ParagraphFormat RightIndent. حسّن تنسيق مستندك اليوم!
type: docs
weight: 280
url: /ar/net/aspose.words/paragraphformat/rightindent/
---
## ParagraphFormat.RightIndent property

يحصل على القيمة (بالنقاط) التي تمثل المسافة البادئة الصحيحة للفقرة أو يعينها.

```csharp
public double RightIndent { get; set; }
```

## أمثلة

يوضح كيفية تكوين تنسيق الفقرة لإنشاء نص خارج المركز.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// قم بتوسيط كل النص الذي يكتبه منشئ المستندات، وقم بإعداد المسافات البادئة.
// سيؤدي تكوين المسافة البادئة أدناه إلى إنشاء مجموعة نصية ستظهر بشكل غير متماثل على الصفحة.
// "المركز" الذي نقوم بمحاذاة النص إليه سيكون منتصف نص الموضوع، وليس منتصف الصفحة.
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
