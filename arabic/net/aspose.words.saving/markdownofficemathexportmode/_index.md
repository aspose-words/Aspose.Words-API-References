---
title: MarkdownOfficeMathExportMode Enum
linktitle: MarkdownOfficeMathExportMode
articleTitle: MarkdownOfficeMathExportMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل Aspose.Words.Saving.MarkdownOfficeMathExportMode على تعزيز تصدير OfficeMath إلى Markdown، مما يضمن تحويل المستندات بدقة وفعالية.
type: docs
weight: 6050
url: /ar/net/aspose.words.saving/markdownofficemathexportmode/
---
## MarkdownOfficeMathExportMode enumeration

يحدد كيفية تصدير Aspose.Words لـ OfficeMath إلى Markdown.

```csharp
public enum MarkdownOfficeMathExportMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Text | `0` | تصدير OfficeMath كنص عادي. |
| Image | `1` | تصدير OfficeMath كصورة. |
| MathML | `2` | تصدير OfficeMath بصيغة MathML. |

## أمثلة

يُظهر كيفية كتابة OfficeMath في المستند.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Saving](../../aspose.words.saving/)
* المجسم [Aspose.Words](../../)
