---
title: MarkdownListExportMode Enum
linktitle: MarkdownListExportMode
articleTitle: MarkdownListExportMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل MarkdownListExportMode الخاص بـ Aspose.Words على تعزيز تصدير القائمة إلى Markdown، مما يضمن التنسيق الدقيق والتكامل السلس لمستنداتك.
type: docs
weight: 6040
url: /ar/net/aspose.words.saving/markdownlistexportmode/
---
## MarkdownListExportMode enumeration

يحدد كيفية تصدير القوائم إلى Markdown.

```csharp
public enum MarkdownListExportMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| MarkdownSyntax | `0` | تصدير عناصر القائمة المتوافقة مع صيغة Markdown. |
| PlainText | `1` | تصدير عناصر القائمة كنص عادي. |

## أمثلة

يوضح كيفية إدراج العناصر التي سيتم كتابتها في مستند Markdown.

```csharp
Document doc = new Document(MyDir + "List item.docx");

// استخدم MarkdownListExportMode.PlainText أو MarkdownListExportMode.MarkdownSyntax لتصدير القائمة.
MarkdownSaveOptions options = new MarkdownSaveOptions { ListExportMode = markdownListExportMode };
doc.Save(ArtifactsDir + "MarkdownSaveOptions.ListExportMode.md", options);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
