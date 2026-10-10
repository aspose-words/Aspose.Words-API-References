---
title: "Aspose::Words::Fonts::FontSubstitutionSettings::get_FontConfigSubstitution 方法"
linktitle: "get_FontConfigSubstitution"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontSubstitutionSettings::get_FontConfigSubstitution 方法。与 C++ 中字体配置替换规则相关的设置。"
type: docs
weight: 3000
url: /zh/cpp/aspose.words.fonts/fontsubstitutionsettings/get_fontconfigsubstitution/
---
## FontSubstitutionSettings::get_FontConfigSubstitution method


[Settings](../../../aspose.words.settings/) related to font config substitution rule.

```cpp
const System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> & Aspose::Words::Fonts::FontSubstitutionSettings::get_FontConfigSubstitution() const
```


## 示例



显示操作系统依赖的字体配置替代。
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// 该 FontConfigSubstitutionRule 对象在 Windows/非 Windows 平台上的工作方式不同。
// 在 Windows 上不可用。
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// 在 Linux/Mac 上，我们可以访问它，并能够执行操作。
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## 另见

* Class [FontConfigSubstitutionRule](../../fontconfigsubstitutionrule/)
* Class [FontSubstitutionSettings](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
