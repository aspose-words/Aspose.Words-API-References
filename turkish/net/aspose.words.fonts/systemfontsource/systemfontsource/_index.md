---
title: SystemFontSource
linktitle: SystemFontSource
articleTitle: SystemFontSource
second_title: .NET için Aspose.Words
description: Verimli font yönetimi için SystemFontSource oluşturucusunu keşfedin. Web tasarımınızı bugün optimize edilmiş tipografi çözümleriyle geliştirin!
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/systemfontsource/systemfontsource/
---
## SystemFontSource() {#constructor}

İşlemci.

```csharp
public SystemFontSource()
```

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

* class [SystemFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)

---

## SystemFontSource(*int*) {#constructor_1}

İşlemci.

```csharp
public SystemFontSource(int priority)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| priority | Int32 | Yazı tipi kaynağı önceliği. Bkz.[`Priority`](../../fontsourcebase/priority/) Daha fazla bilgi için mülk açıklamasına bakın. |

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

* class [SystemFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
