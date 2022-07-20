---
title: HtmlFixedPageHorizontalAlignment
second_title: Aspose.Words for .NET API 参考
description: 指定输出 HTML 文档中页面的水平对齐方式
type: docs
weight: 4810
url: /zh/net/aspose.words.saving/htmlfixedpagehorizontalalignment/
---
## HtmlFixedPageHorizontalAlignment enumeration

指定输出 HTML 文档中页面的水平对齐方式。

```csharp
public enum HtmlFixedPageHorizontalAlignment
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Left | `0` | 将页面向左对齐。 |
| Center | `1` | 居中页面。这是默认值。 |
| Right | `2` | 将页面向右对齐。 |

### 例子

演示如何在将文档保存为 HTML 时设置页面的水平对齐方式。

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

HtmlFixedSaveOptions htmlFixedSaveOptions = new HtmlFixedSaveOptions
{
    PageHorizontalAlignment = pageHorizontalAlignment
};

doc.Save(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment.html", htmlFixedSaveOptions);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlFixedSaveOptions.HorizontalAlignment/styles.css");

switch (pageHorizontalAlignment)
{
    case HtmlFixedPageHorizontalAlignment.Center:
        Assert.True(Regex.Match(outDocContents,
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt auto; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Left:
        Assert.True(Regex.Match(outDocContents, 
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt auto 10pt 10pt; overflow:hidden; }").Success);
        break;
    case HtmlFixedPageHorizontalAlignment.Right:
        Assert.True(Regex.Match(outDocContents, 
            "[.]awpage { position:relative; border:solid 1pt black; margin:10pt 10pt 10pt auto; overflow:hidden; }").Success);
        break;
}
```

### 也可以看看

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving)
* 部件 [Aspose.Words](../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->