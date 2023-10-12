---
title: HtmlLoadOptions.BlockImportMode
second_title: Aspose.Words لمراجع .NET API
description: HtmlLoadOptions ملكية. الحصول على أو تعيين قيمة تحدد كيفية استيراد خصائص عناصر مستوى الكتلة. القيمة الافتراضية هيMerge .
type: docs
weight: 20
url: /ar/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

الحصول على أو تعيين قيمة تحدد كيفية استيراد خصائص عناصر مستوى الكتلة. القيمة الافتراضية هيMerge .

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

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

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* مساحة الاسم [Aspose.Words.Loading](../../htmlloadoptions/)
* المجسم [Aspose.Words](../../../)


