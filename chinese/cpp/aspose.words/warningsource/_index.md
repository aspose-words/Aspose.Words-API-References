---
title: "Aspose::Words::WarningSource 枚举"
linktitle: "WarningSource"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::WarningSource 枚举。指定在 C++ 中文档加载或保存期间产生警告的模块。"
type: docs
weight: 128000
url: /zh/cpp/aspose.words/warningsource/
---
## WarningSource enum


指定在文档加载或保存期间产生警告的模块。

```cpp
enum class WarningSource
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| 未知 | 0 | 未指定警告来源。 |
| 布局 | 1 | 构建文档布局的模块。 |
| DrawingML | 2 | 渲染 DrawingML 形状的模块。 |
| OfficeMath | 3 | 渲染 OfficeMath 的模块。 |
| Shapes | 4 | 渲染普通形状的模块。 |
| Metafile | 5 | 渲染元文件的模块。 |
| Xps | 6 | 渲染 XPS 的模块。 |
| Pdf | 7 | 渲染 PDF 的模块。 |
| 图像 | 8 | 渲染图像的模块。 |
| Docx | 9 | 读取/写入 DOCX 文件的模块。 |
| Doc | 10 | 读取/写入二进制 DOC 文件的模块。 |
| 文本 | 11 | 读取/写入纯文本文件的模块。 |
| Rtf | 12 | 读取/写入 RTF 文件的模块。 |
| WordML | 13 | 读取/写入 WML 文件的模块。 |
| Nrx | 14 | 在 DOCX/WML 读取/写入模块之间共享的通用模块。 |
| Odt | 15 | 读取/写入 ODT 文件的模块。 |
| Html | 16 | 读取/写入 HTML/MHTML 文件的模块。 |
| 验证器 | 17 | 验证模型一致性和有效性的模块。 |
| Xaml | 18 | 读取/写入 Xaml 文件的模块。 |
| Svm | 19 | 读取 Svm 文件的模块。 |
| MathML | 20 | 读取 W3C MathML 文件的模块。 |
| 字体 | 21 | 读取字体文件的模块。 |
| Svg | 22 | 读取 SVG 文件的模块。 |
| Markdown | 23 | 读取/写入 Markdown 文件的模块。 |
| Chm | 24 | 读取 CHM 文件的模块。 |
| Epub | 25 | 读取/写入 EPUB 文件的模块。 |
| Xml | 26 | 读取 XML 文件的模块。 |
| Xlsx | 27 | 写入 XLSX 文件的模块。 |
| Docling | 28 | 写入 Docling JSON 文件的模块。 |


## 示例



展示如何使用警告源。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Emphases markdown warning.docx");

auto warnings = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(warnings);
doc->Save(get_ArtifactsDir() + u"DocumentBuilder.EmphasesWarningSourceMarkdown.md");

for (auto&& warningInfo : warnings)
{
    if (warningInfo->get_Source() == Aspose::Words::WarningSource::Markdown)
    {
        ASSERT_EQ(u"The (*, 0:11) cannot be properly written into Markdown.", warningInfo->get_Description());
    }
}
```


展示如何获取有关字体替换的额外信息。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Rendering.docx");

auto callback = System::MakeObject<Aspose::Words::WarningInfoCollection>();
doc->set_WarningCallback(callback);

auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->SetFontsFolder(get_FontsDir(), false);
fontSettings->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Arial", System::MakeArray<System::String>({u"Arvo", u"Slab"}));

doc->set_FontSettings(fontSettings);
doc->Save(get_ArtifactsDir() + u"FontSettings.SubstitutionWarnings.pdf");

auto warningInfo = System::ExplicitCast<Aspose::Words::FontSubstitutionWarningInfo>(callback->idx_get(0));
ASSERT_EQ(Aspose::Words::WarningSource::Layout, warningInfo->get_Source());
ASSERT_EQ(Aspose::Words::WarningType::FontSubstitution, warningInfo->get_WarningType());
ASSERT_EQ(Aspose::Words::FontSubstitutionReason::TableSubstitutionRule, warningInfo->get_Reason());
ASSERT_EQ(u"Font \'Arial\' has not been found. Using \'Arvo\' font instead. Reason: table substitution.", warningInfo->get_Description());
ASSERT_TRUE(warningInfo->get_RequestedBold());
ASSERT_FALSE(warningInfo->get_RequestedItalic());
ASSERT_EQ(u"Arial", warningInfo->get_RequestedFamilyName());
```

## 另见

* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
