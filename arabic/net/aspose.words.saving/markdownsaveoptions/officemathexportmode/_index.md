---
title: MarkdownSaveOptions.OfficeMathExportMode
linktitle: OfficeMathExportMode
articleTitle: OfficeMathExportMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية MarkdownSaveOptions OfficeMathExportMode لتخصيص مخرجات OfficeMath. حسّن ملفاتك بإعدادات تصدير مرنة!
type: docs
weight: 120
url: /ar/net/aspose.words.saving/markdownsaveoptions/officemathexportmode/
---
## MarkdownSaveOptions.OfficeMathExportMode property

يحدد كيفية كتابة OfficeMath في ملف الإخراج. القيمة الافتراضية هيText .

```csharp
public MarkdownOfficeMathExportMode OfficeMathExportMode { get; set; }
```

## أمثلة

يُظهر كيفية كتابة OfficeMath في المستند.

```csharp
Document doc = new Document(MyDir + "Office math.docx");

MarkdownSaveOptions saveOptions = new MarkdownSaveOptions();
saveOptions.OfficeMathExportMode = MarkdownOfficeMathExportMode.Image;

doc.Save(ArtifactsDir + "MarkdownSaveOptions.OfficeMathExportMode.md", saveOptions);
```

### أنظر أيضا

* enum [MarkdownOfficeMathExportMode](../../markdownofficemathexportmode/)
* class [MarkdownSaveOptions](../)
* مساحة الاسم [Aspose.Words.Saving](../../../aspose.words.saving/)
* المجسم [Aspose.Words](../../../)
