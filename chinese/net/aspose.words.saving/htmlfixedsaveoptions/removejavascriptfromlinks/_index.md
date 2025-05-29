---
title: HtmlFixedSaveOptions.RemoveJavaScriptFromLinks
linktitle: RemoveJavaScriptFromLinks
articleTitle: RemoveJavaScriptFromLinks
second_title: Aspose.Words for .NET
description: 使用 HtmlFixedSaveOptions RemoveJavaScriptFromLinks 功能优化您的 HTML。轻松从链接中删除 JavaScript，增强安全性。
type: docs
weight: 140
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/removejavascriptfromlinks/
---
## HtmlFixedSaveOptions.RemoveJavaScriptFromLinks property

指定是否从链接中删除 JavaScript。 默认值为`错误的`.

```csharp
public bool RemoveJavaScriptFromLinks { get; set; }
```

## 评论

如果启用此选项，所有包含 JavaScript 的链接（例如，href 属性中带有“javascript:”的链接） 将被替换为“javascript:void(0)”。这有助于防止潜在的安全风险，例如 XSS 攻击。

## 例子

展示如何从链接中删除 JavaScript。

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

展示如何从 html 固定文档的链接中删除 JavaScript。

```csharp
Document doc = new Document(MyDir + "JavaScript in HREF.docx");

HtmlFixedSaveOptions saveOptions = new HtmlFixedSaveOptions();
saveOptions.RemoveJavaScriptFromLinks = true;

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.RemoveJavaScriptFromLinks.html", saveOptions);
```

### 也可以看看

* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
