---
title: HtmlSaveOptions.MetafileFormat
linktitle: MetafileFormat
articleTitle: MetafileFormat
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions MetafileFormat 财产. 指定导出为 HTMLMHTML 或 EPUB 时保存图元文件的格式 默认值为Png这意味着图元文件被渲染为光栅 PNG 图像 在 C#.
type: docs
weight: 380
url: /zh/net/aspose.words.saving/htmlsaveoptions/metafileformat/
---
## HtmlSaveOptions.MetafileFormat property

指定导出为 HTML、MHTML 或 EPUB 时保存图元文件的格式。 默认值为Png，这意味着图元文件被渲染为光栅 PNG 图像。

```csharp
public HtmlMetafileFormat MetafileFormat { get; set; }
```

## 评论

HTML 浏览器本身并不显示图元文件。默认情况下，Aspose.Words 在导出为 HTML 时将 WMF 和 EMF 图像转换为 PNG 文件。其他选项是将图元文件转换为 SVG 图像或按原样导出 它们而不进行转换。

如果将元文件图像 导出为 HTML 而不进行转换，则某些图像转换（特别是图像裁剪）将不会应用于图元文件图像。

## 例子

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

* property [ImageResolution](../imageresolution/)
* property [ScaleImageToShapeSize](../scaleimagetoshapesize/)
* enum [HtmlMetafileFormat](../../htmlmetafileformat/)
* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
