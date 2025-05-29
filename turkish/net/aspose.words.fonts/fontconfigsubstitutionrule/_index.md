---
title: FontConfigSubstitutionRule Class
linktitle: FontConfigSubstitutionRule
articleTitle: FontConfigSubstitutionRule
second_title: .NET için Aspose.Words
description: Belgelerinizde kusursuz font yönetimi ve özelleştirmesi için Aspose.Words.Fonts.FontConfigSubstitutionRule sınıfını keşfedin. Metin stilinizi bugün geliştirin!
type: docs
weight: 3300
url: /tr/net/aspose.words.fonts/fontconfigsubstitutionrule/
---
## FontConfigSubstitutionRule class

Yazı tipi yapılandırma değiştirme kuralı.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

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
| [IsFontConfigAvailable](../../aspose.words.fonts/fontconfigsubstitutionrule/isfontconfigavailable/)() | Fontconfig yardımcı programının kullanılabilir olup olmadığını kontrol edin. |
| [ResetCache](../../aspose.words.fonts/fontconfigsubstitutionrule/resetcache/)() | Fontconfig çağrı sonuçlarının önbelleğini sıfırlar. |

## Notlar

Bu kural, orijinal yazı tipi mevcut değilse ikame değerini almak için Linux (ve diğer Unix benzeri) platformlarda fontconfig yardımcı programını kullanır.

Eğer fontconfig yardımcı programı mevcut değilse bu kural göz ardı edilecektir.

## Örnekler

İşletim sistemine bağlı font yapılandırması değişimini gösterir.

```csharp
FontSettings fontSettings = new FontSettings();
FontConfigSubstitutionRule fontConfigSubstitution =
    fontSettings.SubstitutionSettings.FontConfigSubstitution;

bool isWindows = new[] {PlatformID.Win32NT, PlatformID.Win32S, PlatformID.Win32Windows, PlatformID.WinCE}
    .Any(p => Environment.OSVersion.Platform == p);

// FontConfigSubstitutionRule nesnesi Windows/Windows olmayan platformlarda farklı çalışır.
// Windows'ta kullanılamaz.
if (isWindows)
{
    Assert.False(fontConfigSubstitution.Enabled);
    Assert.False(fontConfigSubstitution.IsFontConfigAvailable());
}

bool isLinuxOrMac =
    new[] {PlatformID.Unix, PlatformID.MacOSX}.Any(p => Environment.OSVersion.Platform == p);

// Linux/Mac'te buna erişebileceğiz ve işlemler yapabileceğiz.
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
