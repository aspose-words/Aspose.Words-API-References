---
title: "Aspose::Words::Fonts::SystemFontSource 类"
linktitle: "SystemFontSource"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::SystemFontSource 类。表示系统中安装的所有 TrueType 字体。要了解更多信息，请访问 C++ 文档文章。"
type: docs
weight: 17000
url: /zh/cpp/aspose.words.fonts/systemfontsource/
---
## SystemFontSource class


表示系统中安装的所有 TrueType 字体。欲了解更多，请访问[Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/)文档文章。

```cpp
class SystemFontSource : public Aspose::Words::Fonts::FontSourceBase
```

## 方法

| 方法 | 描述 |
| --- | --- |
| [get_Priority](../fontsourcebase/get_priority/)() const | 返回字体源的优先级。 |
| [get_Type](./get_type/)() override | 返回字体源的类型。 |
| [get_WarningCallback](../fontsourcebase/get_warningcallback/)() const | 在处理字体源时调用，如果检测到可能导致格式保真度损失的问题。 |
| [GetAvailableFonts](../fontsourcebase/getavailablefonts/)() | 返回通过此源可用的字体列表。 |
| static [GetSystemFontFolders](./getsystemfontfolders/)() | 返回系统字体文件夹，如果文件夹不可访问则返回空数组。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [set_WarningCallback](../fontsourcebase/set_warningcallback/)(const System::SharedPtr\<Aspose::Words::IWarningCallback\>\&) | 在处理字体源时调用，如果检测到可能导致格式保真度损失的问题。 |
| [SystemFontSource](./systemfontsource/)() | 构造函数。 |
| [SystemFontSource](./systemfontsource/)(int32_t) | 构造函数。 |
| static [Type](./type/)() |  |

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

* Class [FontSourceBase](../fontsourcebase/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
