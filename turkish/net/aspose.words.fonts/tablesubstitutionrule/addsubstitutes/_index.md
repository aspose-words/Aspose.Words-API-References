---
title: TableSubstitutionRule.AddSubstitutes
second_title: Aspose.Words for .NET API Referansı
description: TableSubstitutionRule yöntem. Verilen orijinal yazı tipi adı için yedek yazı tipi adları ekler.
type: docs
weight: 10
url: /tr/net/aspose.words.fonts/tablesubstitutionrule/addsubstitutes/
---
## TableSubstitutionRule.AddSubstitutes method

Verilen orijinal yazı tipi adı için yedek yazı tipi adları ekler.

```csharp
public void AddSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| originalFontName | String | Orijinal yazı tipi adı. |
| substituteFontNames | String[] | Alternatif yazı tipi adlarının listesi. |

### Örnekler

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

// Windows Yazı Tipleri dizininde var olmayan bir yazı tipinin yerine bir yazı tipi ayarlayın.
doc.FontSettings.SubstitutionSettings.FontInfoSubstitution.Enabled = true;
doc.FontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Kreon-Regular", new[] {"Calibri"});

Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
Assert.Contains("Calibri",
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").ToArray());

// Alternatif olarak, ilgili klasörün yazı tipini içerdiği bir klasör yazı tipi kaynağı ekleyebiliriz.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
doc.FontSettings.SetFontsSources(new FontSourceBase[] {systemFontSource, folderFontSource});
Assert.AreEqual(2, doc.FontSettings.GetFontsSources().Length);

// Yazı tipi kaynaklarını sıfırlamak, bizi hala sistem yazı tipi kaynağının yanı sıra yedeklerimiz ile baş başa bırakır.
doc.FontSettings.ResetFontSources();

Assert.AreEqual(1, doc.FontSettings.GetFontsSources().Length);
Assert.AreEqual(FontSourceType.SystemFonts, doc.FontSettings.GetFontsSources()[0].Type);
Assert.AreEqual(1,
    doc.FontSettings.SubstitutionSettings.TableSubstitution.GetSubstitutes("Kreon-Regular").Count());
```

Özel yazı tipi değiştirme tablolarıyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Yeni bir tablo değiştirme kuralı oluşturun ve varsayılan Windows yazı tipi değiştirme tablosunu yükleyin.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Yazı tiplerini yalnızca klasörümüzden seçersek, özel bir ikame tablosuna ihtiyacımız olacak.
// Artık Microsoft Windows yazı tiplerine erişimimiz olmayacak,
// yeni font klasörümüzde bulunmadığı için "Arial" veya "Times New Roman" gibi.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Aşağıda, yerel dosya sistemindeki bir dosyadan bir ikame tablosu yüklemenin iki yolu bulunmaktadır.
// 1 - Bir akıştan:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Doğrudan bir dosyadan:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Artık "Arial" a erişimimiz olmadığı için, yazı tipi tablomuz önce onu "Varolmayan Yazı Tipi" ile değiştirmeyi deneyecek.
// "MyFonts" klasöründe bulunan bir sonraki "Kreon" yerine geçecek şekilde bu yazı tipine sahip değiliz.
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Bu tabloyu programlı olarak genişletebiliriz. "Times New Roman" yerine "Arvo" yazan bir giriş ekleyeceğiz.
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// AddSubstitutes() ile mevcut bir yazı tipi girişi için ikincil bir geri dönüş ikamesi ekleyebiliriz.
// "Arvo"nun kullanılamaması durumunda, tablomuz ikinci bir ikame seçeneği olarak "M+ 2m"yi arayacaktır.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes(), bir yazı tipi için yeni bir yedek yazı tipi listesi ayarlayabilir.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Erişimimiz olmayan yazı tiplerinde metin yazmak, ikame kurallarımızı çağıracaktır.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Ayrıca bakınız

* class [TableSubstitutionRule](../)
* ad alanı [Aspose.Words.Fonts](../../tablesubstitutionrule/)
* toplantı [Aspose.Words](../../../)


