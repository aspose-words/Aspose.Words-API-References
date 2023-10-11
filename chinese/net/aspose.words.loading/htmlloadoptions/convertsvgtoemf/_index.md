---
title: HtmlLoadOptions.ConvertSvgToEmf
second_title: Aspose.Words for .NET API 参考
description: HtmlLoadOptions 财产. 获取或设置一个值该值指示是否将加载的 SVG 图像转换为 EMF 格式 默认值为错误的并且如果可能加载的 SVG 图像将按原样存储无需转换
type: docs
weight: 30
url: /zh/net/aspose.words.loading/htmlloadoptions/convertsvgtoemf/
---
## HtmlLoadOptions.ConvertSvgToEmf property

获取或设置一个值，该值指示是否将加载的 SVG 图像转换为 EMF 格式。 默认值为`错误的`并且，如果可能，加载的 SVG 图像将按原样存储，无需转换。

```csharp
public bool ConvertSvgToEmf { get; set; }
```

### 评论

MS Word 的较新版本本身支持 SVG 图像。如果加载选项中指定的 MS Word 版本支持 SVG，Aspose.Words 将按原样存储 SVG 图像而不进行转换。如果不支持 SVG，加载的 SVG 图像将被 转换为 EMF 格式。

但是，如果此选项设置为`真的` 即使指定版本的 MS Word 支持 SVG 图像，Aspose.Words 也会将加载的 SVG 图像转换为 EMF。

### 例子

演示如何在保存 HTML 文档时将 SVG 对象转换为其他格式。

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// 使用 'ConvertSvgToEmf' 恢复旧行为
// 从 HTML 文档加载的所有 SVG 图像都被转换为 EMF。
// 现在加载 SVG 图像而不进行转换
// 如果加载选项中指定的 MS Word 版本本身支持 SVG 图像。
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// 该文档包含一个 <svg>;文本形式的元素。
// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象
// 确定保存操作如何处理该对象。
// 将“MetafileFormat”属性设置为“HtmlMetafileFormat.Png”以将其转换为 PNG 图像。
// 将“MetafileFormat”属性设置为“HtmlMetafileFormat.Svg”将其保留为 SVG 对象。
// 将“MetafileFormat”属性设置为“HtmlMetafileFormat.EmfOrWmf”以将其转换为图元文件。
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
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" 版本=\"1.1\" 宽度=\"499\" 高度= \"40\">"));
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
* 命名空间 [Aspose.Words.Loading](../../htmlloadoptions/)
* 部件 [Aspose.Words](../../../)


