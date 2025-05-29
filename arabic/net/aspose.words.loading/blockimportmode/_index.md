---
title: BlockImportMode Enum
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words لـ .NET
description: اكتشف كيف يعمل Aspose.Words.BlockImportMode enum على تعزيز تكامل مستند HTML من خلال تحسين استيراد خصائص العناصر على مستوى الكتلة لتحقيق سير عمل سلس.
type: docs
weight: 4010
url: /ar/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

يحدد كيفية استيراد خصائص عناصر مستوى الكتلة من المستندات المستندة إلى HTML.

```csharp
public enum BlockImportMode
```

### قيم

| اسم | قيمة | وصف |
| --- | --- | --- |
| Merge | `0` | يتم دمج خصائص الكتل الأصلية وتخزينها في العناصر الفرعية (أي الفقرات أو الجداول). |
| Preserve | `1` | يتم استيراد خصائص الكتل الأصلية إلى بنية منطقية خاصة وتخزينها بشكل منفصل عن عقد المستند x000d. |

## أمثلة

يوضح كيفية استيراد خصائص عناصر مستوى الكتلة من المستندات المستندة إلى HTML.

```csharp
const string html = @"
<html>
    <div style='border:dotted'>
        <div style='border:solid'>
            <p>paragraph 1</p>
            <p>paragraph 2</p>
        </div>
    </div>
</html>";
MemoryStream stream = new MemoryStream(Encoding.UTF8.GetBytes(html));

HtmlLoadOptions loadOptions = new HtmlLoadOptions();
// تعيين الوضع الجديد لاستيراد عناصر مستوى كتلة HTML.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)
