---
title: FontSubstitutionSettings Class
linktitle: FontSubstitutionSettings
articleTitle: FontSubstitutionSettings
second_title: .NET için Aspose.Words
description: Verimli font yönetimi için Aspose.Words.Fonts.FontSubstitutionSettings'i keşfedin. Özelleştirilebilir font değiştirme seçenekleriyle belge oluşturmayı optimize edin.
type: docs
weight: 3440
url: /tr/net/aspose.words.fonts/fontsubstitutionsettings/
---
## FontSubstitutionSettings class

Yazı tipi değiştirme mekanizması ayarlarını belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

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

## Notlar

Font değiştirme işlemi belirli bir sırayla tek tek kontrol edilen birkaç kuraldan oluşur. Eğer ilk kural fontu çözemezse ikinci kural kontrol edilir ve bu şekilde devam eder.

Kuralların sırası şu şekildedir: 1. Yazı tipi adı değiştirme kuralı (varsayılan olarak etkindir) 2. Yazı tipi yapılandırma değiştirme kuralı (varsayılan olarak devre dışıdır) 3. Tablo değiştirme kuralı (varsayılan olarak etkindir) 4. Yazı tipi bilgisi değiştirme kuralı (varsayılan olarak etkindir) 5. Varsayılan yazı tipi kuralı (varsayılan olarak etkindir)

Yazı tipi bilgisi değiştirme kuralının, yazı tipini her zaman çözeceğini unutmayın.[`FontInfo`](../fontinfo/) available ve varsayılan yazı tipi kuralını geçersiz kılacaktır. Varsayılan yazı tipi kuralını kullanmak istiyorsanız o zaman yazı tipi bilgisi değiştirme kuralını devre dışı bırakmalısınız.

Font yapılandırma ikame kuralının çoğu durumda fontu çözeceğini ve dolayısıyla diğer tüm kuralları geçersiz kılacağını unutmayın.

## Örnekler

Bir belgenin sistem yazı tipi kaynağına nasıl erişileceğini ve yazı tipi ikamelerinin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
doc.FontSettings = new FontSettings();

// Varsayılan olarak, boş bir belge her zaman bir sistem yazı tipi kaynağı içerir.
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

// Windows Yazı Tipleri dizininde var olan bir yazı tipini, olmayan bir yazı tipinin yerine kullan.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// Alternatif olarak, yazı tipini içeren ilgili klasörün bulunduğu bir yazı tipi kaynağı klasörü ekleyebiliriz.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Yazı tipi kaynaklarını sıfırlamak bize sistem yazı tipi kaynağının yanı sıra yedeklerimizi de bırakır.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.True(doc.FontSettings.SubstitutionSettings.FontNameSubstitution.Enabled);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
