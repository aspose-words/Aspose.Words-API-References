---
title: LoadOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET
description: 探索 LoadOptions Encoding 属性，轻松管理 HTML TXT 或 CHM 文档编码。自定义内容加载，获得最佳性能！
type: docs
weight: 50
url: /zh/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

获取或设置用于加载 HTML、TXT 或 CHM 文档的编码（如果未在文档中指定编码）。 可以是`无效的` 默认为`无效的`.

```csharp
public Encoding Encoding { get; set; }
```

## 评论

此属性仅在加载 HTML、TXT 或 CHM 文档时使用。

如果文档中未指定编码，并且此属性`无效的`，则系统将尝试自动检测编码。

## 例子

展示如何设置打开文档的编码。

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// 在传递 LoadOptions 对象的同时加载文档，然后验证文档的内容。
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
