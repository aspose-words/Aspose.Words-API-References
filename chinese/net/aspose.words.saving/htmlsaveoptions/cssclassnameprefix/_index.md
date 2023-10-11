---
title: HtmlSaveOptions.CssClassNamePrefix
second_title: Aspose.Words for .NET API 参考
description: HtmlSaveOptions 财产. 指定添加到所有 CSS 类名称的前缀 默认值为空字符串生成的 CSS 类名称没有公共前缀
type: docs
weight: 30
url: /zh/net/aspose.words.saving/htmlsaveoptions/cssclassnameprefix/
---
## HtmlSaveOptions.CssClassNamePrefix property

指定添加到所有 CSS 类名称的前缀。 默认值为空字符串，生成的 CSS 类名称没有公共前缀。

```csharp
public string CssClassNamePrefix { get; set; }
```

### 例外

| 例外 | （健康）状况 |
| --- | --- |
| ArgumentException | 该值不为空，并且不是有效的 CSS 标识符。 |

### 评论

如果该值不为空，则 Aspose.Words 生成的所有 CSS 类都将以指定的前缀开头。 这可能很有用，例如，如果您将自定义 CSS 添加到生成的文档并希望防止 class 名称冲突。

如果该值不是`无效的`或者为空，它必须是有效的 CSS 标识符。

### 例子

演示如何将文档保存为 HTML，并向其所有 CSS 类名称添加前缀。

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

Assert.True(outDocContents.Contains(".myprefix-Footer { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n" +
                                    ".myprefix-Header { margin-bottom:0pt; line-height:normal; font-family:Arial; font-size:11pt }\r\n"));
```

### 也可以看看

* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlsaveoptions/)
* 部件 [Aspose.Words](../../../)


