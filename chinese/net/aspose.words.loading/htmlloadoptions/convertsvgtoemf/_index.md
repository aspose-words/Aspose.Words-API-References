---
title: HtmlLoadOptions.ConvertSvgToEmf
linktitle: ConvertSvgToEmf
articleTitle: ConvertSvgToEmf
second_title: Aspose.Words for .NET
description: 探索 HtmlLoadOptions 的 ConvertSvgToEmf 属性。轻松控制 SVG 到 EMF 的转换，以获得最佳图像质量。默认值为 false；保持 SVG 格式完整！
type: docs
weight: 30
url: /zh/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

获取或设置一个值，指示是否将加载的 SVG 图像转换为 EMF 格式。 默认值为`错误的`并且，如果可能的话，加载的 SVG 图像将按原样存储，无需转换。

```csharp
public bool ConvertSvgToEmf { get; set; }
```

## 评论

较新版本的 MS Word 原生支持 SVG 图像。如果加载选项中指定的 MS Word 版本支持 SVG，Aspose.Words 将直接存储 SVG 图像，无需转换。如果不支持 SVG，加载的 SVG 图像将被转换为 EMF 格式。

但是，如果将此选项设置为`真的`，即使指定版本的 MS Word 支持 SVG 图像，Aspose.Words 也会将加载的 SVG 图像转换为 EMF。

## 例子

展示如何在保存 HTML 文档时将 SVG 对象转换为不同的格式。

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// 使用“ConvertSvgToEmf”恢复旧行为
// 其中从 HTML 文档加载的所有 SVG 图像都被转换为 EMF。
// 现在 SVG 图像无需转换即可加载
// 如果加载选项中指定的 MS Word 版本本身支持 SVG 图像。
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// 本文档包含文本形式的 <svg> 元素。
// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象
// 确定保存操作如何处理该对象。
// 将“MetafileFormat”属性设置为“HtmlMetafileFormat.Png”以将其转换为 PNG 图像。
// 将“MetafileFormat”属性设置为“HtmlMetafileFormat.Svg”将其保存为 SVG 对象。
// 将“MetafileFormat”属性设置为“HtmlMetafileFormat.EmfOrWmf”以将其转换为元文件。
HtmlSaveOptions options = new HtmlSaveOptions { MetafileFormat = htmlMetafileFormat };

doc.Save(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.MetafileFormat.html");

switch (htmlMetafileFormat)
{
    case HtmlMetafileFormat.Png:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.png\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
    case HtmlMetafileFormat.Svg:
        Assert.True(outDocContents.Contains(
            "<span style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\">" +
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" 版本=\"1.1\" 宽度=\"499\" 高度=\"40\">"));
        break;
    case HtmlMetafileFormat.EmfOrWmf:
        Assert.True(outDocContents.Contains(
            "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
                "<img src=\"HtmlSaveOptions.MetafileFormat.001.emf\" width=\"500\" height=\"40\" alt=\"\" " +
                "style=\"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>"));
        break;
}
```

### 也可以看看

* class [HtmlLoadOptions](../)
* 命名空间 [Aspose.Words.Loading](../../../aspose.words.loading/)
* 部件 [Aspose.Words](../../../)
