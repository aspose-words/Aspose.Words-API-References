---
title: HtmlInsertOptions Enum
linktitle: HtmlInsertOptions
articleTitle: HtmlInsertOptions
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.HtmlInsertOptions 枚举以使用 InsertHtml 方法自定义 HTML 插入，从而提高文档处理效率。
type: docs
weight: 3570
url: /zh/net/aspose.words/htmlinsertoptions/
---
## HtmlInsertOptions enumeration

指定[`InsertHtml`](../documentbuilder/inserthtml/)方法.

```csharp
[Flags]
public enum HtmlInsertOptions
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| None | `0` | 插入 HTML 时使用默认选项。 |
| UseBuilderFormatting | `1` | 使用指定的字体和段落格式[`DocumentBuilder`](../documentbuilder/)作为从 HTML 插入的 text 的基本格式。 |
| RemoveLastEmptyParagraph | `2` | 删除通常插入在以块级元素结尾的 HTML 之后的空段落。 |
| PreserveBlocks | `4` | 保留块级元素的属性。 |

## 例子

展示如何更好地保留可见的边框和边距。

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

// 设置导入 HTML 块级元素的新模式。
HtmlInsertOptions insertOptions = HtmlInsertOptions.PreserveBlocks;

DocumentBuilder builder = new DocumentBuilder();
builder.InsertHtml(html, insertOptions);
builder.Document.Save(ArtifactsDir + "DocumentBuilder.PreserveBlocks.docx");
```

### 也可以看看

* 命名空间 [Aspose.Words](../../aspose.words/)
* 部件 [Aspose.Words](../../)
