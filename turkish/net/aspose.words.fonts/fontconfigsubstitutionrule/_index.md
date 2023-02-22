---
title: Class FontConfigSubstitutionRule
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fonts.FontConfigSubstitutionRule sınıf. Yazı tipi yapılandırma değiştirme kuralı.
type: docs
weight: 2710
url: /tr/net/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class

Yazı tipi yapılandırma değiştirme kuralı.

```csharp
public class FontConfigSubstitutionRule : FontSubstitutionRule
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| override [Enabled](../../aspose.words.fonts/fontconfigsubstitutionrule/enabled/) { set; } | Kuralın etkin olup olmadığını belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [IsFontConfigAvailable](../../aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/)() | fontconfig yardımcı programının kullanılabilir olup olmadığını kontrol edin. |
| [ResetCache](../../aspose.words.fonts/fontconfigsubstitutionrule/resetcache/)() | fontconfig arama sonuçlarının önbelleğini sıfırlar. |

### Notlar

Bu kural, orijinal yazı tipi mevcut değilse ikame almak için Linux (ve diğer Unix benzeri) platformlarda fontconfig yardımcı programını kullanır.

Eğer fontconfig yardımcı programı yoksa bu kural yok sayılır.

### Örnekler

İşletim sistemine bağlı yazı tipi yapılandırma değişikliğini gösterir.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// FontConfigSubstitutionRule nesnesi, Windows/Windows olmayan platformlarda farklı çalışır.
// Windows'ta kullanılamaz.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// Linux/Mac'te ona erişimimiz olacak ve işlemler yapabileceğiz.
if (isLinuxOrMac)
{
    Assert.True(fontConfigSubstitution.Enabled);
    Assert.True(fontConfigSubstitution.IsFontConfigAvailable());

    fontConfigSubstitution.ResetCache();
}
```

### Ayrıca bakınız

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)


