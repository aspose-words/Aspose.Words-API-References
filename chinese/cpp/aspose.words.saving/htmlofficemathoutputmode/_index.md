---
title: "Aspose::Words::Saving::HtmlOfficeMathOutputMode enum"
linktitle: "HtmlOfficeMathOutputMode"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlOfficeMathOutputMode 枚举。指定 Aspose.Words 在 C++ 中如何将 OfficeMath 导出为 HTML、MHTML 和 EPUB。"
type: docs
weight: 61000
url: /zh/cpp/aspose.words.saving/htmlofficemathoutputmode/
---
## HtmlOfficeMathOutputMode enum


指定 Aspose.Words 如何将 OfficeMath 导出为 HTML、MHTML 和 EPUB。

```cpp
enum class HtmlOfficeMathOutputMode
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 图像 | 0 | OfficeMath 被转换为 HTML，使用 <img> 标签指定的图像。 |
| MathML | 1 | OfficeMath 被转换为使用 MathML 的 HTML。 |
| 文本 | 2 | OfficeMath 被转换为 HTML，作为由 <span> 标签指定的一系列运行。 |


## 示例



展示如何指定将 Microsoft OfficeMath 对象导出为 HTML。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Office math.docx");

// 当我们将文档保存为 HTML 时，可以传入一个 SaveOptions 对象
// 用于确定保存操作如何处理 OfficeMath 对象。
// 将 "OfficeMathOutputMode" 属性设置为 "HtmlOfficeMathOutputMode.Image"
// 将把每个 OfficeMath 对象渲染为图像。
// 将 "OfficeMathOutputMode" 属性设置为 "HtmlOfficeMathOutputMode.MathML"
// 将把每个 OfficeMath 对象转换为 MathML。
// 将 "OfficeMathOutputMode" 属性设置为 "HtmlOfficeMathOutputMode.Text"
// 将使用纯 HTML 文本表示每个 OfficeMath 公式。
auto options = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>();
options->set_OfficeMathOutputMode(htmlOfficeMathOutputMode);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.OfficeMathOutputMode.html", options);
System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.OfficeMathOutputMode.html");

switch (htmlOfficeMathOutputMode)
{
    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::Image:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\"margin-top:0pt; margin-bottom:10pt\">") + u"<img src=\"HtmlSaveOptions.OfficeMathOutputMode.001.png\" width=\"163\" height=\"19\" alt=\"\" style=\"vertical-align:middle; " + u"-aw-left-pos:0pt; -aw-rel-hpos:column; -aw-rel-vpos:paragraph; -aw-top-pos:0pt; -aw-wrap-type:inline\" />" + u"</p>")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::MathML:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\"margin-top:0pt; margin-bottom:10pt; text-align:center\">") + u"<math xmlns=\"http://www.w3.org/1998/Math/MathML\">" + u"<mi>i</mi>" + u"<mo>[+]</mo>" + u"<mi>b</mi>" + u"<mo>-</mo>" + u"<mi>c</mi>" + u"<mo>≥</mo>" + u".*" + u"</math>" + u"</p>")->get_Success());
        break;

    case Aspose::Words::Saving::HtmlOfficeMathOutputMode::Text:
        ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"<p style=\\\"margin-top:0pt; margin-bottom:10pt; text-align:center\\\">") + u"<span style=\\\"font-family:'Cambria Math'\\\">i[+]b-c≥iM[+]bM-cM </span>" + u"</p>")->get_Success());
        break;

}
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
