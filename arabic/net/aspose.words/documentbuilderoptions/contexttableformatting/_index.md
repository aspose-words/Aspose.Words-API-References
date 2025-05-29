---
title: DocumentBuilderOptions.ContextTableFormatting
linktitle: ContextTableFormatting
articleTitle: ContextTableFormatting
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية ContextTableFormatting في DocumentBuilderOptions. تأكد من استقلالية تنسيق الجدول، مما يُحسّن وضوح مستندك وأسلوبه.
type: docs
weight: 20
url: /ar/net/aspose.words/documentbuilderoptions/contexttableformatting/
---
## DocumentBuilderOptions.ContextTableFormatting property

صحيح إذا كان التنسيق المطبق على محتوى الجدول لا يؤثر على تنسيق المحتوى الذي يليه. القيمة الافتراضية هي`حقيقي` .

```csharp
public bool ContextTableFormatting { get; set; }
```

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

* class [DocumentBuilderOptions](../)
* مساحة الاسم [Aspose.Words](../../../aspose.words/)
* المجسم [Aspose.Words](../../../)
