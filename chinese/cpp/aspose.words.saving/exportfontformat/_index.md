---
title: "Aspose::Words::Saving::ExportFontFormat 枚举"
linktitle: "ExportFontFormat"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::ExportFontFormat 枚举。指示在 C++ 中渲染为 HTML 固定格式时用于导出字体的格式。"
type: docs
weight: 54000
url: /zh/cpp/aspose.words.saving/exportfontformat/
---
## ExportFontFormat enum


指示在渲染为 HTML 固定格式时用于导出字体的格式。

```cpp
enum class ExportFontFormat
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| Woff | 0 | WOFF（Web Open [Font](../../aspose.words/font/) 格式）。 |
| Ttf | 1 | TTF（TrueType [Font](../../aspose.words/font/) 格式）。 |


## 示例



展示如何在将文档保存为 HTML 时仅使用目标机器上的字体。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Bullet points with alternative font.docx");

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlFixedSaveOptions>();
saveOptions->set_ExportEmbeddedCss(true);
saveOptions->set_UseTargetMachineFonts(useTargetMachineFonts);
saveOptions->set_FontFormat(Aspose::Words::Saving::ExportFontFormat::Ttf);
saveOptions->set_ExportEmbeddedFonts(false);

doc->Save(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UsingMachineFonts.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlFixedSaveOptions.UsingMachineFonts.html");

if (useTargetMachineFonts)
{
    ASSERT_FALSE(System::Text::RegularExpressions::Regex::Match(outDocContents, u"@font-face")->get_Success());
}
else
{
    ASSERT_TRUE(System::Text::RegularExpressions::Regex::Match(outDocContents, System::String(u"@font-face { font-family:'Arial'; font-style:normal; font-weight:normal; src:local[(]'☺'[)], ") + u"url[(]'HtmlFixedSaveOptions.UsingMachineFonts/font001.ttf'[)] format[(]'truetype'[)]; }")->get_Success());
}
```

## 另见

* Namespace [Aspose::Words::Saving](../)
* Library [Aspose.Words for C++](../../)
