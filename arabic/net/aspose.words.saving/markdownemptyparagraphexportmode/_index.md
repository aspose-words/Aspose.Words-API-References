---
title: MarkdownEmptyParagraphExportMode Enum
linktitle: MarkdownEmptyParagraphExportMode
articleTitle: MarkdownEmptyParagraphExportMode
second_title: Aspose.Words لـ .NET
description: تعرّف على كيفية تعامل Aspose.Words مع الفقرات الفارغة في تصدير Markdown. تحكّم في التنسيق باستخدام MarkdownEmptyParagraphExportMode enum.
type: docs
weight: 6010
url: /ar/net/aspose.words.saving/markdownemptyparagraphexportmode/
---
## MarkdownEmptyParagraphExportMode enumeration

يحدد كيفية تصدير Aspose.Words للفقرات الفارغة إلى Markdown.

```csharp
public enum MarkdownEmptyParagraphExportMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| EmptyLine | `0` | تصدير كأسطر فارغة. |
| MarkdownHardLineBreak | `1` | تصدير كحرف Markdown HardLineBreak '\'. |
| None | `2` | لا تقم بتصدير الفقرات الفارغة. |

## أمثلة

يوضح كيفية تصدير الفقرات الفارغة.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("First");
builder.Writeln("\r\n\r\n\r\n");
builder.Writeln("Last");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.EmptyParagraphExportMode = exportMode;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.EmptyParagraphExportMode.md", saveOptions);

string result = File.ReadAllText(ArtifactsDir + "MarkdownSaveOptions.EmptyParagraphExportMode.md");

switch (exportMode)
{
    case MarkdownEmptyParagraphExportMode.None:
        Assert.AreEqual("First\r\n\r\nLast\r\n", result);
        break;
    case MarkdownEmptyParagraphExportMode.EmptyLine:
        Assert.AreEqual("First\r\n\r\n\r\n\r\n\r\nLast\r\n\r\n", result);
        break;
    case MarkdownEmptyParagraphExportMode.MarkdownHardLineBreak:
        Assert.AreEqual("First\r\n\\\r\n\\\r\n\\\r\n\\\r\n\\\r\nLast\r\n<br>\r\n", result);
        break;
}
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
