---
title: SystemFontSource
linktitle: SystemFontSource
articleTitle: SystemFontSource
second_title: Aspose.Words for .NET
description: SystemFontSource inşaatçı. Ctor C#'da.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/systemfontsource/systemfontsource/
---
## SystemFontSource() {#constructor}

Ctor.

```csharp
public SystemFontSource()
```

## Örnekler

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

* class [SystemFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)

---

## SystemFontSource(*int*) {#constructor_1}

Ctor.

```csharp
public SystemFontSource(int priority)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| priority | Int32 | Yazı tipi kaynağı önceliği. Bkz.[`Priority`](../../fontsourcebase/priority/) Daha fazla bilgi için özellik açıklaması. |

## Örnekler

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

* class [SystemFontSource](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
