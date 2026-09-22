---
title: "Aspose::Words::Fonts::FontConfigSubstitutionRule class"
linktitle: "FontConfigSubstitutionRule"
second_title: "C++ için Aspose.Words API Referansı"
description: "Aspose::Words::Fonts::FontConfigSubstitutionRule sınıfı. Yazı tipi yapılandırma ikamesi kuralı. Daha fazla bilgi için C++'taki belge makalesini ziyaret edin."
type: docs
weight: 4000
url: /tr/cpp/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class


[Font](../../aspose.words/font/) config substitution rule. To learn more, visit the [Working with Fonts](https://docs.aspose.com/words/cpp/working-with-fonts/) documentation article.

```cpp
class FontConfigSubstitutionRule : public Aspose::Words::Fonts::FontSubstitutionRule
```

## Yöntemler

| Yöntem | Açıklama |
| --- | --- |
| virtual [get_Enabled](../fontsubstitutionrule/get_enabled/)() | Kuralın etkin olup olmadığını belirtir. |
| [GetType](./gettype/)() const override |  |
| [Is](./is/)(const System::TypeInfo\&) const override |  |
| [IsFontConfigAvailable](./isfontconfigavailable/)() | fontconfig aracının mevcut olup olmadığını kontrol edin. |
| [ResetCache](./resetcache/)() | fontconfig çağrı sonuçlarının önbelleğini sıfırlar. |
| [set_Enabled](./set_enabled/)(bool) override | Kuralın etkin olup olmadığını belirtir. |
| static [Type](./type/)() |  |
## Açıklamalar


Bu kural, orijinal yazı tipi mevcut değilse ikameyi elde etmek için Linux (ve diğer Unix benzeri) platformlarda fontconfig aracını kullanır.

fontconfig aracı mevcut değilse bu kural yok sayılacaktır.

## Örnekler



İşletim sistemi bağımlı yazı tipi yapılandırma ikamesini gösterir.
```cpp
auto fontSettings = System::MakeObject<Aspose::Words::Fonts::FontSettings>();
System::SharedPtr<Aspose::Words::Fonts::FontConfigSubstitutionRule> fontConfigSubstitution = fontSettings->get_SubstitutionSettings()->get_FontConfigSubstitution();

bool isWindows = System::MakeArray<System::PlatformID>({System::PlatformID::Win32NT, System::PlatformID::Win32S, System::PlatformID::Win32Windows, System::PlatformID::WinCE})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// FontConfigSubstitutionRule nesnesi Windows/Windows dışı platformlarda farklı çalışır.
// Windows'ta kullanılamaz.
if (isWindows)
{
    ASSERT_FALSE(fontConfigSubstitution->get_Enabled());
    ASSERT_FALSE(fontConfigSubstitution->IsFontConfigAvailable());
}

bool isLinuxOrMac = System::MakeArray<System::PlatformID>({System::PlatformID::Unix, System::PlatformID::MacOSX})->LINQ_Any(static_cast<System::Func<System::PlatformID, bool>>(static_cast<std::function<bool(System::PlatformID p)>>([](System::PlatformID p) -> bool
{
    return System::Environment::get_OSVersion().get_Platform() == p;
})));

// Linux/Mac'te ona erişebileceğiz ve işlemler yapabileceğiz.
if (isLinuxOrMac)
{
    ASSERT_TRUE(fontConfigSubstitution->get_Enabled());
    ASSERT_TRUE(fontConfigSubstitution->IsFontConfigAvailable());

    fontConfigSubstitution->ResetCache();
}
```

## Ayrıca Bakınız

* Class [FontSubstitutionRule](../fontsubstitutionrule/)
* Namespace [Aspose::Words::Fonts](../)
* Library [Aspose.Words for C++](../../)
