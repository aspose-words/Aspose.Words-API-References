---
title: HtmlOfficeMathOutputMode Enum
linktitle: HtmlOfficeMathOutputMode
articleTitle: HtmlOfficeMathOutputMode
second_title: Aspose.Words for .NET
description: 了解 Aspose.Words.Saving.HtmlOfficeMathOutputMode 如何增强 OfficeMath 导出到 HTML、MHTML 和 EPUB 的功能，实现无缝文档转换。
type: docs
weight: 5850
url: /zh/net/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enumeration

指定 Aspose.Words 如何将 OfficeMath 导出为 HTML、MHTML 和 EPUB。

```csharp
public enum HtmlOfficeMathOutputMode
```

### 价值观

| 姓名 | 价值 | 描述 |
| --- | --- | --- |
| Image | `0` | OfficeMath 转换为 HTML，作为 &lt;img&gt; 标签指定的图像。 |
| MathML | `1` | OfficeMath 使用 MathML 转换为 HTML。 |
| Text | `2` | OfficeMath 被转换为 HTML，作为由 &lt;span&gt; 标签指定的运行序列。 |

## 例子

展示如何指定如何将 Microsoft OfficeMath 对象导出为 HTML。

```csharp
Document doc = new Document(MyDir + "Office math.docx");

// 当我们将文档保存为 HTML 时，我们可以传递一个 SaveOptions 对象
// 确定保存操作如何处理 OfficeMath 对象。
// 将“OfficeMathOutputMode”属性设置为“HtmlOfficeMathOutputMode.Image”
// 将把每个 OfficeMath 对象渲染成一个图像。
// 将“OfficeMathOutputMode”属性设置为“HtmlOfficeMathOutputMode.MathML”
// 将把每个 OfficeMath 对象转换为 MathML。
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
                "<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"163\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " +
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

* 命名空间 [Aspose.Words.Saving](../../aspose.words.saving/)
* 部件 [Aspose.Words](../../)
