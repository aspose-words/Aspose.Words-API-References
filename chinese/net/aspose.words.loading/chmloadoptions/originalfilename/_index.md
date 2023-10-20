---
title: ChmLoadOptions.OriginalFileName
linktitle: OriginalFileName
articleTitle: OriginalFileName
second_title: 用于 .NET 的 Aspose.Words
description: ChmLoadOptions OriginalFileName 财产. CHM 文件的名称 默认值为无效的 在 C#.
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

CHM 文档可能包含按文件名引用同一文档的链接。 Aspose.Words 支持这样的 links 并且通常使用[`OriginalFileName`](../../../aspose.words/document/originalfilename/)检查 link 引用的文件是否是正在加载的文件。如果从流中加载文档，则应通过此属性明确指定其原始文件名 ，因为它无法自动确定。

如果从文件中加载 CHM 文档并为此属性指定了非空值，则该值将优先于 中存储的文件的实际名称[`OriginalFileName`](../../../aspose.words/document/originalfilename/).

## 例子

展示如何解析诸如“ms-its:myfile.chm::/index.htm”之类的 URL。

```csharp
// 我们的文档包含像“ms-its:amhelp.chm::....htm”这样的 URL，但它有不同的名称，
// 所以文件链接在保存为 HTML 后不起作用。
// 我们需要在 'ChmLoadOptions' 中定义原始文件名以避免这种行为。
ChmLoadOptions loadOptions = new ChmLoadOptions { OriginalFileName = "amhelp.chm" };

Document doc = new Document(new MemoryStream(File.ReadAllBytes(MyDir + "Document with ms-its links.chm")),
    loadOptions);

doc.Save(ArtifactsDir + "ExChmLoadOptions.OriginalFileName.html");
```

### 也可以看看

* class [ChmLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
