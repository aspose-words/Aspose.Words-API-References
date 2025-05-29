---
title: MergeFormatMode Enum
linktitle: MergeFormatMode
articleTitle: MergeFormatMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية Aspose.Words.LowCode.MergeFormatMode لتحسين دمج المستندات. حسّن التحكم في التنسيق عند دمج ملفات متعددة بسهولة.
type: docs
weight: 4290
url: /ar/net/aspose.words.lowcode/mergeformatmode/
---
## MergeFormatMode enumeration

يحدد كيفية دمج التنسيق عند الجمع بين مستندات متعددة.

```csharp
public enum MergeFormatMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| MergeFormatting | `0` | دمج تنسيق المستندات المدمجة. |
| KeepSourceFormatting | `1` | يعني أن المستند المصدر سيحتفظ بتنسيقه الأصلي، مثل أنماط الخطوط وأحجامها وألوانها والمسافات البادئة وأي عناصر تنسيق أخرى يتم تطبيقها على محتواه. |
| KeepSourceLayout | `2` | الحفاظ على تخطيط المستندات الأصلية في المستند النهائي. |

## أمثلة

يوضح كيفية دمج المستندات في مستند إخراج واحد.

```csharp
//هناك عدة طرق لدمج المستندات:
string inputDoc1 = MyDir + "Big document.docx";
string inputDoc2 = MyDir + "Tables.docx";

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.1.docx", new[] { inputDoc1, inputDoc2 });

OoxmlSaveOptions saveOptions = new OoxmlSaveOptions { Password = "Aspose.Words" };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.2.docx", new[] { inputDoc1, inputDoc2 }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.3.pdf", new[] { inputDoc1, inputDoc2 }, SaveFormat.Pdf, MergeFormatMode.KeepSourceLayout);

LoadOptions firstLoadOptions = new LoadOptions() { IgnoreOleData = true };
LoadOptions secondLoadOptions = new LoadOptions() { IgnoreOleData = false };
Merger.Merge(ArtifactsDir + "LowCode.MergeDocument.4.docx", new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, saveOptions, MergeFormatMode.KeepSourceFormatting);

Document doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.5.docx");

doc = Merger.Merge(new[] { inputDoc1, inputDoc2 }, new[] { firstLoadOptions, secondLoadOptions }, MergeFormatMode.MergeFormatting);
doc.Save(ArtifactsDir + "LowCode.MergeDocument.6.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.LowCode](../../aspose.words.lowcode/)
* المجسم [Aspose.Words](../../)
