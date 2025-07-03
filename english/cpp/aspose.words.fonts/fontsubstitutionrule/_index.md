---
title: Aspose::Words::Fonts::FontSubstitutionRule class
linktitle: FontSubstitutionRule
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontSubstitutionRule class. This is an abstract base class for the font substitution rule. To learn more, visit the  documentation article in C++.'
type: docs
weight: 12000
url: /cpp/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class


This is an abstract base class for the font substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontSubstitutionRule : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [get_Enabled](./get_enabled/)() | Specifies whether the rule is enabled or not. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| virtual [set_Enabled](./set_enabled/)(bool) | Setter for [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](./get_enabled/). |
| static [Type](./type/)() |  |

## Examples



Shows operating system-dependent font config substitution. 
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// The FontConfigSubstitutionRule object works differently on Windows/non-Windows platforms.
// On Windows, it is unavailable.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// On Linux/Mac, we will have access to it, and will be able to perform operations.
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## See Also

* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
