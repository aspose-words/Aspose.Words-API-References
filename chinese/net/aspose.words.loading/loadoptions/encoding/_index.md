---
title: LoadOptions.Encoding
second_title: Aspose.Words for .NET API 参考
description: LoadOptions 财产. 获取或设置将用于加载 HTMLTXT 或 CHM 文档的编码如果未指定编码 在文档内部 可以无效的默认为无效的.
type: docs
weight: 50
url: /zh/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

获取或设置将用于加载 HTML、TXT 或 CHM 文档的编码（如果未指定编码） 在文档内部。 可以`无效的`。默认为`无效的`.

```csharp
public Encoding Encoding { get; set; }
```

### 评论

此属性仅在加载 HTML、TXT 或 CHM 文档时使用。

如果文档内未指定编码且此属性为`无效的`，那么系统会尝试to 自动检测编码。

### 例子

演示如何设置打开文档所用的编码。

```csharp
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.ASCII
};

// 在传递 LoadOptions 对象时加载文档，然后验证文档的内容。
Document doc = new Document(MyDir + "English text.txt", loadOptions);

Assert.True(doc.ToString(SaveFormat.Text).Contains("This is a sample text in English."));
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../loadoptions/)
* 部件 [Aspose.Words](../../../)


