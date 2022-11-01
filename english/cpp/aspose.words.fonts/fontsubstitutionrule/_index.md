---
title: FontSubstitutionRule
second_title: Aspose.Words for C++ API Reference
description: This is an abstract base class for the font substitution rule.
type: docs
weight: 144
url: /cpp/aspose.words.fonts/fontsubstitutionrule/
---
## FontSubstitutionRule class


This is an abstract base class for the font substitution rule.

```cpp
class FontSubstitutionRule : public System::Object
```

## Methods

| Method | Description |
| --- | --- |
| virtual [get_Enabled](./get_enabled/)() | Specifies whether the rule is enabled or not. |
| virtual [set_Enabled](./set_enabled/)(bool) | Setter for [Aspose::Words::Fonts::FontSubstitutionRule::get_Enabled](./get_enabled/). |

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

