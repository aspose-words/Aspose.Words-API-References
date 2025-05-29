---
title: BlockImportMode Enum
linktitle: BlockImportMode
articleTitle: BlockImportMode
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words.BlockImportMode 枚举如何通过优化块级元素属性导入实现无缝工作流程，从而增强 HTML 文档集成。
type: docs
weight: 4010
url: /zh/net/aspose.words.loading/blockimportmode/
---
## BlockImportMode enumeration

指定如何从基于 HTML 的文档导入块级元素的属性。

```csharp
public enum BlockImportMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Merge | `0` | 父块的属性被合并并存储在子元素（即段落或表格）上。 |
| Preserve | `1` | 父块的属性被导入到特殊的逻辑结构中，并与 文档节点分开存储。 |

## 例子

展示如何从基于 HTML 的文档导入块级元素的属性。

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

* 命名空间 [Aspose.Words.Loading](../../aspose.words.loading/)
* 部件 [Aspose.Words](../../)
