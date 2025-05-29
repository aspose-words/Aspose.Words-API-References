---
title: MarkdownLinkExportMode Enum
linktitle: MarkdownLinkExportMode
articleTitle: MarkdownLinkExportMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل Aspose.Words MarkdownLinkExportMode enum على تعزيز تصدير الروابط في Markdown، مما يعمل على تحسين عملية تحويل المستندات لديك بسهولة.
type: docs
weight: 6030
url: /ar/net/aspose.words.saving/markdownlinkexportmode/
---
## MarkdownLinkExportMode enumeration

يحدد كيفية تصدير الروابط إلى Markdown.

```csharp
public enum MarkdownLinkExportMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Auto | `0` | الكشف تلقائيًا عن وضع التصدير لكل رابط. |
| Inline | `1` | تصدير جميع الروابط ككتل مضمنة. |
| Reference | `2` | تصدير جميع الروابط ككتل مرجعية. |

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

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
