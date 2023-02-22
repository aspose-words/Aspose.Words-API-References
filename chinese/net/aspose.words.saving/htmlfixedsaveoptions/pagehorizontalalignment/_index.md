---
title: HtmlFixedSaveOptions.PageHorizontalAlignment
second_title: Aspose.Words for .NET API 参考
description: HtmlFixedSaveOptions 财产. 指定 HTML 文档中页面的水平对齐方式 默认值为HtmlFixedHorizontalPageAlignment.Center.
type: docs
weight: 110
url: /zh/net/aspose.words.saving/htmlfixedsaveoptions/pagehorizontalalignment/
---
## HtmlFixedSaveOptions.PageHorizontalAlignment property

指定 HTML 文档中页面的水平对齐方式。 默认值为`HtmlFixedHorizontalPageAlignment.Center`.

```csharp
public HtmlFixedPageHorizontalAlignment PageHorizontalAlignment { get; set; }
```

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

* enum [HtmlFixedPageHorizontalAlignment](../../htmlfixedpagehorizontalalignment/)
* class [HtmlFixedSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../htmlfixedsaveoptions/)
* 部件 [Aspose.Words](../../../)


