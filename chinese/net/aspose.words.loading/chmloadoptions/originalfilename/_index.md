---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: Aspose.Words for .NET
description: 探索 ChmLoadOptions OriginalFileName 属性，轻松设置 CHM 文件名，简化访问流程。默认值为 null。优化您的体验！
type: docs
weight: 20
url: /zh/net/aspose.words.loading/chmloadoptions/originalfilename/
---
## ChmLoadOptions.OriginalFileName property

CHM 文件的名称。 默认值为`无效的`.

```csharp
public string OriginalFileName { get; set; }
```

## 评论

CHM 文档可能包含通过文件名引用同一文档的链接。Aspose.Words 支持此类链接 并且通常使用[`OriginalFileName`](../../../aspose.words/document/originalfilename/)检查链接引用的文件是否是正在加载的文件。如果文档是从流中加载的，则应通过此属性明确指定其原始文件名，因为无法自动确定。

如果从文件加载 CHM 文档，并且指定了此属性的非空值，则该值将优先于存储在[`OriginalFileName`](../../../aspose.words/document/originalfilename/).

## 例子

展示如何解析类似“ms-its:myfile.chm::/index.htm”的 URL。

```csharp
// 我们的文档包含类似“ms-its:amhelp.chm::....htm”的 URL，但它有不同的名称，
// 因此将文件保存为 HTML 后，文件链接不起作用。
// 我们需要在“ChmLoadOptions”中定义原始文件名以避免这种行为。
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### 也可以看看

* class [ChmLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
