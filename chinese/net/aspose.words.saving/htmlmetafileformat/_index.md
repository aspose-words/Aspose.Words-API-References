---
title: HtmlMetafileFormat Enum
linktitle: HtmlMetafileFormat
articleTitle: HtmlMetafileFormat
second_title: Aspose.Words for .NET
description: 探索 Aspose.Words.Saving.HtmlMetafileFormat 枚举，实现在 HTML 文档中无缝保存元文件。立即提升您的文档转换体验！
type: docs
weight: 5840
url: /zh/net/aspose.words.saving/htmlmetafileformat/
---
## HtmlMetafileFormat enumeration

表示元文件保存为 HTML 文档的格式。

```csharp
public enum HtmlMetafileFormat
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Png | `0` | 元文件被渲染为光栅 PNG 图像。 |
| Svg | `1` | 元文件转换为矢量 SVG 图像。 |
| EmfOrWmf | `2` | 图元文件按原样保存，无需转换。 |

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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
