---
title: Aspose::Words::Fonts::FontConfigSubstitutionRule class
linktitle: FontConfigSubstitutionRule
second_title: Aspose.Words for C++ API Reference
description: 'Aspose::Words::Fonts::FontConfigSubstitutionRule class. Font config substitution rule. To learn more, visit the  documentation article in C++.'
type: docs
weight: 4000
url: /cpp/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class


[Font](../../aspose.words/font/) config substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontConfigSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Methods

| Method | Description |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Specifies whether the rule is enabled or not. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsFontConfigAvailable](./isfontconfigavailable/)() | Check if fontconfig utility is available or not. |
| [ResetCache](./resetcache/)() | Resets the cache of fontconfig calling results. |
| [set_Enabled](./set_enabled/)(bool) override | Specifies whether the rule is enabled or not. |
| static [Type](./type/)() |  |
## Remarks


This rule uses fontconfig utility on Linux (and other Unix-like) platforms to get the substitution if the original font is not available.

If fontconfig utility is not available then this rule will be ignored.

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

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
