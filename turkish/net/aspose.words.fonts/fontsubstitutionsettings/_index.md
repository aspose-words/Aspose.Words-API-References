---
title: Class FontSubstitutionSettings
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Fonts.FontSubstitutionSettings sınıf. Yazı tipi değiştirme mekanizması ayarlarını belirtir.
type: docs
weight: 3010
url: /tr/net/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class

Yazı tipi değiştirme mekanizması ayarlarını belirtir.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Fontlarla Çalışmak](https://docs.aspose.com/words/net/working-with-fonts/) dokümantasyon makalesi.

```csharp
public class FontSubstitutionSettings
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [DefaultFontSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/defaultfontsubstitution/) { get; } | Varsayılan yazı tipi değiştirme kuralıyla ilgili ayarlar. |
| [FontConfigSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontconfigsubstitution/) { get; } | Yazı tipi yapılandırma değiştirme kuralıyla ilgili ayarlar. |
| [FontInfoSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontinfosubstitution/) { get; } | Yazı tipi bilgisi değiştirme kuralıyla ilgili ayarlar. |
| [FontNameSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/fontnamesubstitution/) { get; } | Yazı tipi adı değiştirme kuralıyla ilgili ayarlar. |
| [TableSubstitution](../../aspose.words.fonts/fontsubstitutionsettings/tablesubstitution/) { get; } | Tablo değiştirme kuralıyla ilgili ayarlar. |

### Notlar

Yazı tipi değiştirme işlemi belirli bir sırayla tek tek kontrol edilen birçok kuraldan oluşur. İlk kural yazı tipini çözemezse ikinci kural kontrol edilir ve bu şekilde devam eder.

Kuralların sırası şu şekildedir: 1. Yazı tipi adı değiştirme kuralı (varsayılan olarak etkindir) 2. Yazı tipi yapılandırması değiştirme kuralı (varsayılan olarak devre dışıdır) 3. Tablo değiştirme kuralı (varsayılan olarak etkindir) 4. Yazı tipi bilgisi değiştirme kuralı (varsayılan olarak etkindir) 5. Varsayılan yazı tipi kuralı (varsayılan olarak etkindir)

Yazı tipi bilgisi değiştirme kuralının aşağıdaki durumlarda yazı tipini her zaman çözeceğini unutmayın:[`FontInfo`](../fontinfo/) kullanılabilir 'dir ve varsayılan yazı tipi kuralını geçersiz kılar. Varsayılan yazı tipi kuralını kullanmak istiyorsanız the yazı tipi bilgisi değiştirme kuralını devre dışı bırakmalısınız.

Yazı tipi yapılandırma değiştirme kuralının çoğu durumda yazı tipini çözeceğini ve dolayısıyla diğer tüm kuralları geçersiz kılacağını unutmayın.

### Örnekler

Bir belgenin sistem yazı tipi kaynağına nasıl erişileceğini ve yazı tipi yedeklerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// Varsayılan olarak boş bir belge her zaman bir sistem yazı tipi kaynağı içerir.
Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);

SystemFontSource systemFontSource = (SystemFontSource) doc.FontSettings.GetFontsSources()[0];
Assert.AreEqual(FontSourceType.SystemFonts, systemFontSource.Type);
Assert.AreEqual(0, systemFontSource.Priority);

PlatformID pid = Environment.OSVersion.Platform;
bool isWindows = (pid == PlatformID.Win32NT) || (pid == PlatformID.Win32S) ||
                 (pid == PlatformID.Win32Windows) || (pid == PlatformID.WinCE);
if (isWindows)
{
    const string fontsPath = @"C:\WINDOWS\Fonts";
    Assert.AreEqual(fontsPath.ToLower(),
        SystemFontSource.GetSystemFontFolders().FirstOrDefault()?.ToLower());
}

foreach (string systemFontFolder in SystemFontSource.GetSystemFontFolders())
{
    Console.WriteLine(systemFontFolder);
}

// Windows Yazı Tipleri dizininde bulunan bir yazı tipini, bulunmayan bir yazı tipinin yerine ayarlayın.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// Alternatif olarak, karşılık gelen klasörün yazı tipini içerdiği bir klasör yazı tipi kaynağı ekleyebiliriz.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Yazı tipi kaynaklarını sıfırlamak bizi yine de sistem yazı tipi kaynağı ve yedeklerimizle baş başa bırakır.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)


