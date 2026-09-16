---
title: "Aspose::Words::Fonts::FontSubstitutionSettings class"
linktitle: "FontSubstitutionSettings"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontSubstitutionSettings class. 指定字体替换机制的设置。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 13000
url: /zh/cpp/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class


指定字体替换机制的设置。欲了解更多，请访问[Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/)文档文章。

```cpp
class FontSubstitutionSettings : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_DefaultFontSubstitution](./get_defaultfontsubstitution/)() const | [Settings](../../aspose.words.settings/) 与默认字体替换规则相关。 |
| [get_FontConfigSubstitution](./get_fontconfigsubstitution/)() const | [Settings](../../aspose.words.settings/) 与字体配置替换规则相关。 |
| [get_FontInfoSubstitution](./get_fontinfosubstitution/)() const | [Settings](../../aspose.words.settings/) 与字体信息替换规则相关。 |
| [get_FontNameSubstitution](./get_fontnamesubstitution/)() const | [Settings](../../aspose.words.settings/) 与字体名称替换规则相关。 |
| [get_TableSubstitution](./get_tablesubstitution/)() const | [Settings](../../aspose.words.settings/) 与表格替换规则相关。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| static [Type](./type/)() |  |
## 备注


[Font](../../aspose.words/font/) substitution process consists of several rules which are checked one by one in specific order. If the first rule can't resolve the font then second rule is checked and so on.

规则的顺序如下：1. [Font](../../aspose.words/font/) 名称替换规则（默认启用）
1. [Font](../../aspose.words/font/) 配置替换规则（默认禁用）
1. 表格替换规则（默认启用）
1. [Font](../../aspose.words/font/) 信息替换规则（默认启用）
1. 默认字体规则（默认启用）



请注意，如果存在 [FontInfo](../fontinfo/)，字体信息替换规则将始终解析该字体，并会覆盖默认字体规则。若想使用默认字体规则，则应禁用字体信息替换规则。

请注意，字体配置替换规则在大多数情况下会解析字体，从而覆盖所有其他规则。

## 示例



展示如何访问文档的系统字体源并设置字体替代。
```cpp
auto doc = System::MakeObject<Aspose::Words::Document>();
doc->set_FontSettings(System::MakeObject<Aspose::Words::Fonts::FontSettings>());

// 默认情况下，空白文档始终包含系统字体源。
ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());

auto systemFontSource = System::ExplicitCast<Aspose::Words::Fonts::SystemFontSource>(doc->get_FontSettings()->GetFontsSources()->idx_get(0));
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, systemFontSource->get_Type());
ASSERT_EQ(0, systemFontSource->get_Priority());

System::PlatformID pid = System::Environment::get_OSVersion().get_Platform();
bool isWindows = (pid == System::PlatformID::Win32NT) || (pid == System::PlatformID::Win32S) || (pid == System::PlatformID::Win32Windows) || (pid == System::PlatformID::WinCE);
if (isWindows)
{
    const System::String fontsPath = u"C:\\WINDOWS\\Fonts";
    System::String actual = System::Default<System::String>();
    System::String condExpression = Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders()->LINQ_FirstOrDefault();
    if (condExpression != nullptr)
    {
        actual = condExpression.ToLower();
    }
    ASSERT_EQ(fontsPath.ToLower(), actual);
}

for (System::String systemFontFolder : Aspose::Words::Fonts::SystemFontSource::GetSystemFontFolders())
{
    std::cout << systemFontFolder << std::endl;
}

// 将 Windows 字体目录中存在的字体设置为不存在的字体的替代品。
doc->get_FontSettings()->get_SubstitutionSettings()->get_FontInfoSubstitution()->set_Enabled(true);
doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->AddSubstitutes(u"Kreon-Regular", System::MakeArray<System::String>({u"Calibri"}));

ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_ToArray()->Contains(u"Calibri"));

// 或者，我们可以添加一个文件夹字体源，其中相应的文件夹包含该字体。
auto folderFontSource = System::MakeObject<Aspose::Words::Fonts::FolderFontSource>(get_FontsDir(), false);
doc->get_FontSettings()->SetFontsSources(System::MakeArray<System::SharedPtr<Aspose::Words::Fonts::FontSourceBase>>({systemFontSource, folderFontSource}));
ASSERT_EQ(2, doc->get_FontSettings()->GetFontsSources()->get_Length());

// 重置字体源后仍会保留系统字体源以及我们的替代字体。
doc->get_FontSettings()->ResetFontSources();

ASSERT_EQ(1, doc->get_FontSettings()->GetFontsSources()->get_Length());
ASSERT_EQ(Aspose::Words::Fonts::FontSourceType::SystemFonts, doc->get_FontSettings()->GetFontsSources()->idx_get(0)->get_Type());
ASSERT_EQ(1, doc->get_FontSettings()->get_SubstitutionSettings()->get_TableSubstitution()->GetSubstitutes(u"Kreon-Regular")->LINQ_Count());
ASSERT_TRUE(doc->get_FontSettings()->get_SubstitutionSettings()->get_FontNameSubstitution()->get_Enabled());
```

## 另见

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
