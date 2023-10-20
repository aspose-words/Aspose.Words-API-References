---
title: HtmlSaveOptions.OfficeMathOutputMode
linktitle: OfficeMathOutputMode
articleTitle: OfficeMathOutputMode
second_title: 用于 .NET 的 Aspose.Words
description: HtmlSaveOptions OfficeMathOutputMode 财产. 控制 OfficeMath 对象如何导出为 HTMLMHTML 或 EPUB 默认值为HtmlOfficeMathOutputMode.Image 在 C#.
type: docs
weight: 400
url: /zh/net/aspose.words.saving/htmlsaveoptions/officemathoutputmode/
---
## HtmlSaveOptions.OfficeMathOutputMode property

控制 OfficeMath 对象如何导出为 HTML、MHTML 或 EPUB。 默认值为`HtmlOfficeMathOutputMode.Image`.

```csharp
public HtmlOfficeMathOutputMode OfficeMathOutputMode { get; set; }
```

## 例子

演示如何指定如何将 Microsoft OfficeMath 对象导出为 HTML。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象
// 确定保存操作如何处理 OfficeMath 对象。
// 将“OfficeMathOutputMode”属性设置为“HtmlOfficeMathOutputMode.Image”
// 将每个 OfficeMath 对象渲染成图像。
// 将“OfficeMathOutputMode”属性设置为“HtmlOfficeMathOutputMode.MathML”
// 将每个 OfficeMath 对象转换为 MathML。
// 将“OfficeMathOutputMode”属性设置为“HtmlOfficeMathOutputMode.Text”
// 将使用纯 HTML 文本表示每个 OfficeMath 公式。
HtmlSaveOptions options = new HtmlSaveOptions { OfficeMathOutputMode = htmlOfficeMathOutputMode };

doc.Save(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html", options);
string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
    case HtmlOfficeMathOutputMode.Image:
        Assert.True(Regex.Match(outDocContents, 
            "<p style=\"margin-top:0pt; margin-bottom:10pt\">" +
                "<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"159\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " +
                "-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" +
            "</p>").Success);
        break;
    case HtmlOfficeMathOutputMode.MathML:
        Assert.True(Regex.Match(outDocContents,
            "<p style=\"margin-top:0pt; margin-bottom:10pt; text-align:center\">" +
                "<math xmlns=\"http://www.w3.org/1998/Math/MathML\">" +
                    "<mi>i</mi>" +
                    "<mo>[+]</mo>" +
                    "<mi>b</mi>" +
                    "<mo>-</mo>" +
                    "<mi>c</mi>" +
                    "<mo>≥</mo>" +
                    ".*" +
                "</math>" +
            "</p>").Success);
        break;
    case HtmlOfficeMathOutputMode.Text:
        Assert.True(Regex.Match(outDocContents,
            @"<p style=\""margin-top:0pt; margin-bottom:10pt; text-align:center\"">" +
                @"<span style=\""font-family:'Cambria Math'\"">i[+]b-c≥iM[+]bM-cM </span>" +
            "</p>").Success);
        break;
}
```

### 也可以看看

* enum [HtmlOfficeMathOutputMode](../../htmlofficemathoutputmode/)
* class [HtmlSaveOptions](../)
* 命名空间 [Aspose.Words.Saving](../../../aspose.words.saving/)
* 部件 [Aspose.Words](../../../)
