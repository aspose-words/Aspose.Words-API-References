---
title: HtmlLoadOptions.BlockImportMode
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: 用于 .NET 的 Aspose.Words
description: HtmlLoadOptions BlockImportMode 财产. 获取或设置一个值该值指定如何导入块级元素的属性 默认值为Merge 在 C#.
type: docs
weight: 20
url: /zh/net/aspose.words.loading/htmlloadoptions/blockimportmode/
---
## HtmlLoadOptions.BlockImportMode property

获取或设置一个值，该值指定如何导入块级元素的属性。 默认值为Merge.

```csharp
public BlockImportMode BlockImportMode { get; set; }
```

## 例子

显示如何从基于 HTML 的文档导入块级元素的属性。

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
// 设置导入 HTML 块级元素的新模式。
loadOptions.BlockImportMode = blockImportMode;

Document doc = new Document(stream, loadOptions);
doc.Save(ArtifactsDir + "HtmlLoadOptions.BlockImport.docx");
```

### 也可以看看

* enum [BlockImportMode](../../blockimportmode/)
* class [HtmlLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
