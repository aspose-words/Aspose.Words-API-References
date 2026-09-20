---
title: "Aspose::Words::FontSubstitutionReason 枚举"
linktitle: "FontSubstitutionReason"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FontSubstitutionReason 枚举。指定 C++ 中字体替换的原因。"
type: docs
weight: 89500
url: /zh/cpp/aspose.words/fontsubstitutionreason/
---
## FontSubstitutionReason enum


指定字体替换的原因。

```cpp
enum class FontSubstitutionReason
```

### 值

| 名称 | 值 | 描述 |
| --- | --- | --- |
| AlternativeName | 0 | [Font](../font/) 替换为文档中的备用名称。 |
| FontNameSubstitutionRule | 1 | [Font](../font/) 替换依据字体名称规则。 |
| FontConfigSubstitutionRule | 2 | [Font](../font/) 替换依据字体配置规则。 |
| TableSubstitutionRule | 3 | [Font](../font/) 替换依据表格规则。 |
| FontInfoSubstitutionRule | 4 | [Font](../font/) 替换依据字体信息规则。 |
| DefaultFontSubstitutionRule | 5 | [Font](../font/) 替换依据默认字体规则。 |
| FirstAvailableFont | 6 | [Font](../font/) 替换为第一个可用的字体。 |


## 示例



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
