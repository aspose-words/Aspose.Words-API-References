---
title: Enum BlockImportMode
second_title: Aspose.Words لمراجع .NET API
description: Aspose.Words.Loading.BlockImportMode تعداد. يحدد كيفية استيراد خصائص عناصر مستوى الكتلة من المستندات المستندة إلى HTML.
type: docs
weight: 3560
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
| Merge | `0` | يتم دمج خصائص الكتل الرئيسية وتخزينها في العناصر الفرعية (أي الفقرات أو الجداول). |
| Preserve | `1` | يتم استيراد خصائص الكتل الأصلية إلى بنية منطقية خاصة ويتم تخزينها بشكل منفصل عن عقد الوثيقة. |

### أمثلة

يوضح كيفية استيراد خصائص العناصر على مستوى الكتلة من المستندات المستندة إلى HTML.

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
// قم بتعيين الوضع الجديد لاستيراد عناصر مستوى كتلة HTML.
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### أنظر أيضا

* مساحة الاسم [Aspose.Words.Loading](../../aspose.words.loading/)
* المجسم [Aspose.Words](../../)


