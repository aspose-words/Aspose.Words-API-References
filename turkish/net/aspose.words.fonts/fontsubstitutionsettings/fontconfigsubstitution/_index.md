---
title: FontSubstitutionSettings.FontConfigSubstitution
second_title: Aspose.Words for .NET API Referansı
description: FontSubstitutionSettings mülk. Yazı tipi yapılandırma değiştirme kuralıyla ilgili ayarlar.
type: docs
weight: 20
url: /tr/net/aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/
---
## FontSubstitutionSettings.FontConfigSubstitution property

Yazı tipi yapılandırma değiştirme kuralıyla ilgili ayarlar.

```csharp
public FontConfigSubstitutionRule FontConfigSubstitution { get; }
```

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

* class [FontConfigSubstitutionRule](../../fontconfigsubstitutionrule/)
* class [FontSubstitutionSettings](../)
* ad alanı [Aspose.Words.Fonts](../../fontsubstitutionsettings/)
* toplantı [Aspose.Words](../../../)


