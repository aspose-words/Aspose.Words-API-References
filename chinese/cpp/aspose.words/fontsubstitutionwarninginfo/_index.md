---
title: "Aspose::Words::FontSubstitutionWarningInfo 类"
linktitle: "FontSubstitutionWarningInfo"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::FontSubstitutionWarningInfo 类。包含有关 Aspose.Words 在 C++ 中加载或保存文档时发出的字体替换警告的信息。"
type: docs
weight: 29500
url: /zh/cpp/aspose.words/fontsubstitutionwarninginfo/
---
## FontSubstitutionWarningInfo class


包含 Aspose.Words 在文档加载或保存期间发出的字体替换警告信息。

```cpp
class FontSubstitutionWarningInfo : public Aspose::Words::WarningInfo
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Description](../warninginfo/get_description/)() const | 返回警告的描述。 |
| [get_Reason](./get_reason/)() const | [Font](../font/) 替换原因。 |
| [get_RequestedBold](./get_requestedbold/)() const | 指示是否请求了粗体样式。 |
| [get_RequestedFamilyName](./get_requestedfamilyname/)() const | 请求的字体族名称。 |
| [get_RequestedItalic](./get_requesteditalic/)() const | 指示是否请求了斜体样式。 |
| [get_ResolvedFont](./get_resolvedfont/)() const | 已解析的字体。 |
| [get_Source](../warninginfo/get_source/)() const | 返回警告的来源。 |
| [get_WarningType](../warninginfo/get_warningtype/)() const | 返回警告的类型。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |

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

* Class [WarningInfo](../warninginfo/)
* Namespace [Aspose::Words](../)
* Library [Aspose.Words for C++](../../)
