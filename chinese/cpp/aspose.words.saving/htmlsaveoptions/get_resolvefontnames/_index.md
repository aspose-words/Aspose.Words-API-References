---
title: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames 方法"
linktitle: "get_ResolveFontNames"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames 方法。指定在 C++ 中将文档写入基于 HTML 的格式时，是否根据 FontSettings 解析并替换文档中使用的字体族名称。"
type: docs
weight: 42000
url: /zh/cpp/aspose.words.saving/htmlsaveoptions/get_resolvefontnames/
---
## HtmlSaveOptions::get_ResolveFontNames method


指定在将文档写入基于 HTML 的格式时，是否根据 [FontSettings](../../../aspose.words/document/get_fontsettings/) 解析并替换文档中使用的字体族名称。

```cpp
bool Aspose::Words::Saving::HtmlSaveOptions::get_ResolveFontNames() const
```

## 备注


默认情况下，此选项设置为 **false**，字体族名称将按照源文档的指定写入 HTML。也就是说，[FontSettings](../../../aspose.words/document/get_fontsettings/) 被忽略，不会对字体族名称进行解析或替换。

如果此选项设置为 **true**，Aspose.Words 将使用 [FontSettings](../../../aspose.words/document/get_fontsettings/) 将源文档中指定的每个字体族名称解析为可用的字体族名称，并根据需要执行字体替换。

## 示例



展示如何在写入 HTML 之前解析所有字体名称。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>(get_MyDir() + u"Missing font.docx");

// 此文档包含提及我们未拥有的字体的文本。
ASSERT_FALSE(System::TestTools::IsNull(doc->get_FontInfos()->idx_get(u"28 Days Later")));

// 如果我们无法获取此字体，并且希望能够显示所有文本
// 在输出的 HTML 中显示此文档时，我们可以用另一种字体进行替换。
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_DefaultFontName(u"Arial");
fontSettings->get_SubstitutionSettings()->get_DefaultFontSubstitution()->set_Enabled(true);

doc->set_FontSettings(fontSettings);

auto saveOptions = System::MakeObject<Aspose::Words::Saving::HtmlSaveOptions>(Aspose::Words::SaveFormat::Html);
// 默认情况下，此选项设置为 'False'，Aspose.Words 会按照源文档的指定写入字体名称
saveOptions->set_ResolveFontNames(resolveFontNames);

doc->Save(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html", saveOptions);

System::String outDocContents = System::IO::File::ReadAllText(get_ArtifactsDir() + u"HtmlSaveOptions.ResolveFontNames.html");

ASSERT_TRUE(resolveFontNames ? System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:Arial\">")->get_Success() : System::Text::RegularExpressions::Regex::Match(outDocContents, u"<span style=\"font-family:\'28 Days Later\'\">")->get_Success());
```

## 另见

* Class [HtmlSaveOptions](../)
* Namespace [Aspose::Words::Saving](../../)
* Library [Aspose.Words for C++](../../../)
