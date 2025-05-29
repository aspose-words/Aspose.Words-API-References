---
title: TableSubstitutionRule.LoadWindowsSettings
linktitle: LoadWindowsSettings
articleTitle: LoadWindowsSettings
second_title: .NET için Aspose.Words
description: LoadWindowsSettings yöntemi ile Windows için önceden tanımlanmış tablo değiştirme ayarlarını zahmetsizce yükleyin. İş akışınızı bugün optimize edin!
type: docs
weight: 60
url: /tr/net/aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/
---
## TableSubstitutionRule.LoadWindowsSettings method

Windows platformu için önceden tanımlanmış tablo değiştirme ayarlarını yükler.

```csharp
public void LoadWindowsSettings()
```

## Örnekler

Windows ve Linux için font değiştirme tablolarına nasıl erişileceğini gösterir.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Yeni bir tablo değiştirme kuralı oluşturun ve varsayılan Microsoft Windows yazı tipi değiştirme tablosunu yükleyin.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;
tableSubstitutionRule.LoadWindowsSettings();

// Windows'ta "Times New Roman CE" yazı tipinin varsayılan alternatifi "Times New Roman"dır.
Assert.AreEqual(new[] {"Times New Roman"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Tabloyu XML belgesi şeklinde kaydedebiliriz.
tableSubstitutionRule.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Windows.xml");

// Linux'un kendine ait bir ikame tablosu vardır.
// "Times New Roman CE" için birden fazla alternatif yazı tipi bulunmaktadır.
// Eğer ilk ikame "FreeSerif" de mevcut değilse,
// bu kural, kullanılabilir bir kural bulana kadar dizideki diğerleri arasında geçiş yapacaktır.
tableSubstitutionRule.LoadLinuxSettings();
Assert.AreEqual(new[] {"FreeSerif", "Liberation Serif", "DejaVu Serif"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman CE").ToArray());

// Linux ikame tablosunu bir akış kullanarak XML belgesi biçiminde kaydedin.
using (FileStream fileStream = new FileStream(ArtifactsDir + "FontSettings.TableSubstitutionRule.Linux.xml",
    FileMode.Create))
{
    tableSubstitutionRule.Save(fileStream);
}
```

### Ayrıca bakınız

* class [TableSubstitutionRule](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
