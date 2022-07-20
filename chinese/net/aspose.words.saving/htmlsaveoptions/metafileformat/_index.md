---
title: MetafileFormat
second_title: Aspose.Words for .NET API 参考
description: 指定导出到 HTMLMHTML 或 EPUB 时元文件的保存格式 默认值为Png这意味着元文件被渲染为光栅 PNG 图像
type: docs
weight: 390
url: /zh/net/aspose.words.saving/htmlsaveoptions/metafileformat/
---
## HtmlSaveOptions.MetafileFormat property

指定导出到 HTML、MHTML 或 EPUB 时元文件的保存格式。 默认值为Png，这意味着元文件被渲染为光栅 PNG 图像。

```csharp
public HtmlMetafileFormat MetafileFormat { get; set; }
```

### 评论

HTML 浏览器本身不会显示元文件。默认情况下，Aspose.Words 在导出为 HTML 时会将 WMF 和 EMF 图像转换为 PNG 文件。其他选项是将元文件转换为 SVG 图像或将它们按原样导出 x000d_ 而不进行转换。

如果将它们 导出为 HTML 而不进行转换，则某些图像转换（尤其是图像裁剪）将不会应用于图元文件图像。

### 例子

展示如何在保存 HTML 文档时将 SVG 对象转换为不同的格式。

```csharp
string html = 
    @"<html>
        <svg xmlns='http://www.w3.org/2000/svg' width='500' height='40' viewBox='0 0 500 40'>
            <text x='0' y='35' font-family='Verdana' font-size='35'>Hello world!</text>
        </svg>
    </html>";

// 使用 'ConvertSvgToEmf' 转回传统行为
// 从 HTML 文档加载的所有 SVG 图像都被转换为 EMF。
// 现在 SVG 图像无需转换即可加载
// 如果加载选项中指定的 MS Word 版本本机支持 SVG 图像。
HtmlLoadOptions loadOptions = new HtmlLoadOptions { ConvertSvgToEmf = true };

Document doc = new Document(new MemoryStream(Encoding.UTF8.GetBytes(html)), loadOptions);

// 这个文档包含一个 <svg>文本形式的元素。
// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象
// 确定保存操作如何处理这个对象。
// 将“MetafileFormat”属性设置为“HtmlMetafileFormat.Png”以将其转换为PNG图像。
// 将“MetafileFormat”属性设置为“HtmlMetafileFormat.Svg”，将其保存为 SVG 对象。
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
            "<svg xmlns=\"http://www.w3.org/2000/svg\" xmlns:xlink=\"http://www.w3.org/1999/xlink\" version=\"1.1\" width=\"499\" height= \"40\">"));
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

* property [ImageResolution](../imageresolution)
* property [ScaleImageToShapeSize](../scaleimagetoshapesize)
* enum [HtmlMetafileFormat](../../htmlmetafileformat)
* class [HtmlSaveOptions](../../htmlsaveoptions)
* 命名空间 [Aspose.Words.Saving](../../htmlsaveoptions)
* 部件 [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->