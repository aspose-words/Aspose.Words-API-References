---
title: Aspose::Words::Fonts::FontConfigSubstitutionRule::IsFontConfigAvailable method
linktitle: IsFontConfigAvailable
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontConfigSubstitutionRule::IsFontConfigAvailable method. Check if fontconfig utility is available or not in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/
---
## FontConfigSubstitutionRule::IsFontConfigAvailable method


Check if fontconfig utility is available or not.

```cpp
bool Aspose::Words::Fonts::FontConfigSubstitutionRule::IsFontConfigAvailable()
```


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

* Class [FontConfigSubstitutionRule](../)
* Namespace [Aspose::Words::Fonts](../../)
* Library [Aspose.Words for C++](../../../)
