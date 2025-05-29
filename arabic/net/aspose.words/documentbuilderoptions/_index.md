---
title: DocumentBuilderOptions Class
linktitle: DocumentBuilderOptions
articleTitle: DocumentBuilderOptions
second_title: Aspose.Words لـ .NET
description: اكتشف خيارات Aspose.Words.DocumentBuilder لتحسين عملية إنشاء المستندات باستخدام ميزات قابلة للتخصيص للحصول على تجربة بناء سلسة.
type: docs
weight: 670
url: /ar/net/aspose.words/documentbuilderoptions/
---
## DocumentBuilderOptions class

يسمح بتحديد خيارات إضافية لعملية بناء المستند.

```csharp
public class DocumentBuilderOptions
```

## المنشئون

| اسم | وصف |
| --- | --- |
| [DocumentBuilderOptions](documentbuilderoptions/)() | Default_Constructor |

## الخصائص

| اسم | وصف |
| --- | --- |
| [ContextTableFormatting](../../aspose.words/documentbuilderoptions/contexttableformatting/) { get; set; } | صحيح إذا كان التنسيق المطبق على محتوى الجدول لا يؤثر على تنسيق المحتوى الذي يليه. القيمة الافتراضية هي`حقيقي` . |
| [DesignMode](../../aspose.words/documentbuilderoptions/designmode/) { get; set; } | يتوافق مع وضع التصميم في Microsoft Word. |

## أمثلة

يوضح كيفية تجاهل تنسيق الجدول للمحتوى بعد ذلك.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

//يضيف المحتوى قبل الجدول.
// حجم الخط الافتراضي هو 12.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
//تغيير حجم الخط داخل الجدول.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// إذا كان ContextTableFormatting صحيحًا، فلن يتم تطبيق تنسيق الجدول على المحتوى بعد ذلك.
// إذا كان ContextTableFormatting خاطئًا، فسيتم تطبيق تنسيق الجدول على المحتوى بعد ذلك.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words](../../aspose.words/)
* المجسم [Aspose.Words](../../)
