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
auto fontSettings = MakeObject<FontSettings>();
SharedPtr<FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

System::PlatformID pid = System::Environment::get_OSVersion().get_Platform();
bool isWindows = (pid == System::PlatformID::Win32NT) || (pid == System::PlatformID::Win32S) || (pid == System::PlatformID::Win32Windows) ||
                 (pid == System::PlatformID::WinCE);

// The FontConfigSubstitutionRule object works differently on Windows/non-Windows platforms.
// On Windows, it is unavailable.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = (pid == System::PlatformID::Unix) || (pid == System::PlatformID::MacOSX);

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
