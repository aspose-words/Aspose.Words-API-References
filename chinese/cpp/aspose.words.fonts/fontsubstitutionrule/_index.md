---
title: "Aspose::Words::Fonts::FontSubstitutionRule 类"
linktitle: "FontSubstitutionRule"
second_title: "Aspose.Words for C++ API 参考"
description: "Aspose::Words::Fonts::FontSubstitutionRule 类。这是字体替代规则的抽象基类。欲了解更多，请访问 C++ 文档文章。"
type: docs
weight: 12000
url: /zh/cpp/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class


这是用于字体替换规则的抽象基类。欲了解更多，请访问[Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/)文档文章。

```cpp
class FontSubstitutionRule : public System::Object
```

## 方法

| 方法 | 描述 |
| --- | --- |
| virtual [get_Enabled](./get_enabled/)() | 指定规则是否已启用。 |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Enabled](./set_enabled/)(bool) | 用于设置 [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](./get_enabled/)。 |
| static [Type](./type/)() |  |

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

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
