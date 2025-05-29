---
title: ChmLoadOptions
linktitle: ChmLoadOptions
articleTitle: ChmLoadOptions
second_title: Aspose.Words for .NET
description: 探索 ChmLoadOptions 构造函数，实现无缝初始化。轻松设置默认值，立即提升应用程序性能！
type: docs
weight: 10
url: /zh/net/aspose.words.loading/chmloadoptions/chmloadoptions/
---
## ChmLoadOptions constructor

使用默认值初始化此类的新实例。

```csharp
public ChmLoadOptions()
```

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
