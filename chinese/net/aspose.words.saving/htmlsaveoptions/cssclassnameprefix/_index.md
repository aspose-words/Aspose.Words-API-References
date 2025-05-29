---
title: HtmlSaveOptions.CssClassNamePrefix
linktitle: CssClassNamePrefix
articleTitle: CssClassNamePrefix
second_title: Aspose.Words for .NET
description: 发现 HtmlSaveOptions CssClassNamePrefix 属性，使用唯一前缀轻松自定义 CSS 类名，增强您的网页设计一致性。
type: docs
weight: 30
url: /zh/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

指定添加到所有 CSS 类名的前缀。 默认值为空字符串，生成的 CSS 类名没有通用前缀。

```csharp
public string CssClassNamePrefix { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentException | 该值不为空并且不是有效的 CSS 标识符。 |

## 评论

如果此值不为空，则 Aspose.Words 生成的所有 CSS 类都将以指定的前缀 开头。这可能会很有用，例如，如果您向生成的文档添加自定义 CSS 并希望防止 class 名称冲突。

如果值不是`无效的`或为空，它必须是一个有效的 CSS 标识符。

## 例子

展示如何将文档保存为 HTML，并为其所有 CSS 类名添加前缀。

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");

HtmlSaveOptions saveOptions = new HtmlSaveOptions
{
    CssStyleSheetType = CssStyleSheetType.External,
    CssClassNamePrefix = "myprefix-"
};

doc.Save(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html", saveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.html");

Assert.True(outDocContents.Contains("<p class=\"myprefix-Header\">"));
Assert.True(outDocContents.Contains("<p class=\"myprefix-Footer\">"));

outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.CssClassNamePrefix.css");

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:footer }"));
Assert.True(outDocContents.Contains(".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt; -aw-style-name:header }"));
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
