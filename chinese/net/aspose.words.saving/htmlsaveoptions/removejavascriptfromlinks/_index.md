---
title: HtmlSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words for .NET
description: 使用 HtmlSaveOptions 优化您的 Web 内容，轻松从链接中删除 JavaScript，提高性能并改善用户体验。
type: docs
weight: 410
url: /zh/net/aspose.words.saving/htmlsaveoptions/removejavascriptfromlinks/
---
## HtmlSaveOptions.RemoveJavaScriptFromLinks property

指定是否从链接中删除 JavaScript。 默认值为`错误的`.

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## 评论

如果启用此选项，所有包含 JavaScript 的链接（例如，href 属性中带有“javascript:”的链接） 将被替换为“javascript:void(0)”。这有助于防止潜在的安全风险，例如 XSS 攻击。

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
