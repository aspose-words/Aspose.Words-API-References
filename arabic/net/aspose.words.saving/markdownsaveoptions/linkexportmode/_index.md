---
title: MarkdownSaveOptions.LinkExportMode
linktitle: LinkExportMode
articleTitle: LinkExportMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MarkdownSaveOptions LinkExportMode للتحكم في تنسيق الروابط في ملفات الإخراج. حسّن تصدير مستنداتك بسهولة!
type: docs
weight: 100
url: /ar/net/aspose.words.saving/markdownsaveoptions/linkexportmode/
---
## MarkdownSaveOptions.LinkExportMode property

يحدد كيفية كتابة الروابط إلى ملف الإخراج. القيمة الافتراضية هيAuto .

```csharp
public MarkdownLinkExportMode LinkExportMode { get; set; }
```

## أمثلة

يوضح كيفية كتابة الروابط إلى ملف .md.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.InsertShape(ShapeType.Balloon, 100, 100);

// سيتم كتابة الصورة كمرجع:
// ![ref1]
//
// [ref1]: aw_ref.001.png
MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.LinkExportMode = MarkdownLinkExportMode.Reference;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Reference.md", saveOptions);

// سيتم كتابة الصورة على هيئة مضمنة:
// ![](aw_inline.001.png)
saveOptions.LinkExportMode = MarkdownLinkExportMode.Inline;
doc.Save(ArtifactsDir + "MarkdownSaveOptions.LinkExportMode.Inline.md", saveOptions);
```

### أنظر أيضا

* enum [MarkdownLinkExportMode](../../markdownlinkexportmode/)
* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
