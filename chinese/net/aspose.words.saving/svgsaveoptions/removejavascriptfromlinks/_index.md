---
title: SvgSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words for .NET
description: 使用 SvgSaveOptions 优化 SVG 文件，轻松移除链接中的 JavaScript，让代码更简洁。只需简单设置，即可提升性能和安全性！
type: docs
weight: 60
url: /zh/net/aspose.words.saving/svgsaveoptions/removejavascriptfromlinks/
---
## SvgSaveOptions.RemoveJavaScriptFromLinks property

指定是否从链接中删除 JavaScript。 默认值为`错误的` . 如果启用此选项，所有包含 JavaScript 的链接都将被替换为“javascript:void(0)”。

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## 例子

展示如何从链接（svg）中删除 JavaScript。

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

SvgSaveOptions saveOptions = new SvgSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "SvgSaveOptions.RemoveJavaScriptFromLinksSvg.html", saveOptions);
```

### 也可以看看

* class [SvgSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
