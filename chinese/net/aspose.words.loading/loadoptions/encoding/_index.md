---
title: LoadOptions.Encoding
second_title: Aspose.Words for .NET API 参考
description: LoadOptions 财产. 获取或设置将用于加载 HTMLTXT 或 CHM 文档的编码如果未在文档中指定编码  可以为空默认为空
type: docs
weight: 50
url: /zh/net/aspose.words.loading/loadoptions/encoding/
---
## LoadOptions.Encoding property

获取或设置将用于加载 HTML、TXT 或 CHM 文档的编码（如果未在文档中指定编码） 。 可以为空。默认为空。

```csharp
public Encoding Encoding { get; set; }
```

### 评论

此属性仅在加载 HTML、TXT 或 CHM 文档时使用。

如果文档中未指定编码并且此属性为`无效的`，然后系统会尝试to 自动检测编码。

### 例子

显示如何设置打开文档的编码。

```csharp
// FileFormatInfo 对象会检测到这个文件是不是用 UTF-7 编码的。
FileFormatInfo fileFormatInfo = FileFormatUtil.DetectFileFormat(MyDir + "Encoded in UTF-7.txt");

Assert.AreNotEqual(Encoding.UTF7, fileFormatInfo.Encoding);

// 如果我们在没有加载配置的情况下加载文档，Aspose.Words 将检测其编码为 UTF-8。
Document doc = new Document(MyDir + "Encoded in UTF-7.txt");

// 以 UTF-8 解析的内容创建一个有效的字符串。
// 但是，知道文件是 UTF-7 的，我们可以看到结果是不正确的。
Assert.AreEqual("Hello world+ACE-", doc.ToString(SaveFormat.Text).Trim());

// 在这种不明确的编码的情况下，我们可以设置一个特定的编码变体
// 在 LoadOptions 对象中解析文件。
LoadOptions loadOptions = new LoadOptions
{
    Encoding = Encoding.UTF7
};

// 在传递 LoadOptions 对象的同时加载文档，然后验证文档的内容。
doc = new Document(MyDir + "Encoded in UTF-7.txt", loadOptions);

Assert.AreEqual("Hello world!", doc.ToString(SaveFormat.Text).Trim());
```

### 也可以看看

* class [LoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../loadoptions/)
* 部件 [Aspose.Words](../../../)


