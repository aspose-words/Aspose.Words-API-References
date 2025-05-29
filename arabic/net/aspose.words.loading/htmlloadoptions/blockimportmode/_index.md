---
title: HtmlLoadOptions.BlockImportMode
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words لـ .NET
description: اكتشف خاصية BlockImportMode في HtmlLoadOptions لتخصيص استيراد العناصر على مستوى الكتلة. تحكّم في الدمج لإدارة مثالية للمحتوى!
type: docs
weight: 20
url: /ar/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

يحصل على قيمة تحدد كيفية استيراد خصائص عناصر مستوى الكتلة أو يعينها. القيمة الافتراضية هيMerge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

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

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../../aspose.words.loading/)
* المجسم [Aspose.Words](../../../)
