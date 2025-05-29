---
title: TableSubstitutionRule Class
linktitle: TableSubstitutionRule
articleTitle: TableSubstitutionRule
second_title: .NET için Aspose.Words
description: Belgelerinizde verimli font yönetimi ve kusursuz metin biçimlendirme için Aspose.Words.Fonts.TableSubstitutionRule sınıfını keşfedin.
type: docs
weight: 3490
url: /tr/net/aspose.words.fonts/tablesubstitutionrule/
---
## TableSubstitutionRule class

Tablo yazı tipi değiştirme kuralı.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public class TableSubstitutionRule : FontSubstitutionRule
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| virtual [Enabled](../../aspose.words.fonts/fontsubstitutionrule/enabled/) { get; set; } | Kuralın etkin olup olmadığını belirtir. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [AddSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/addsubstitutes/)(*string, params string[]*) | Verilen orijinal yazı tipi adı için yedek yazı tipi adları ekler. |
| [GetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/getsubstitutes/)(*string*) | Belirtilen orijinal yazı tipi adı için yedek yazı tipi adlarını içeren diziyi döndürür. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load)(*Stream*) | XML akışından tablo değiştirme ayarlarını yükler. |
| [Load](../../aspose.words.fonts/tablesubstitutionrule/load/#load_1)(*string*) | XML dosyasından tablo değiştirme ayarlarını yükler. |
| [LoadAndroidSettings](../../aspose.words.fonts/tablesubstitutionrule/loadandroidsettings/)() | Android platformu için önceden tanımlanmış tablo değiştirme ayarlarını yükler. |
| [LoadLinuxSettings](../../aspose.words.fonts/tablesubstitutionrule/loadlinuxsettings/)() | Linux platformu için önceden tanımlanmış tablo değiştirme ayarlarını yükler. |
| [LoadWindowsSettings](../../aspose.words.fonts/tablesubstitutionrule/loadwindowssettings/)() | Windows platformu için önceden tanımlanmış tablo değiştirme ayarlarını yükler. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save)(*Stream*) | Mevcut tablo değiştirme ayarlarını akışa kaydeder. |
| [Save](../../aspose.words.fonts/tablesubstitutionrule/save/#save_1)(*string*) | Mevcut tablo değiştirme ayarlarını dosyaya kaydeder. |
| [SetSubstitutes](../../aspose.words.fonts/tablesubstitutionrule/setsubstitutes/)(*string, params string[]*) | Belirtilen orijinal yazı tipi adı için yedek yazı tipi adlarını geçersiz kıl. |

## Notlar

Bu kural, orijinal yazı tipi mevcut değilse kullanılacak yedek yazı tipi adlarının listesini tanımlar. Yazı tipi adı için yedekler kontrol edilecek ve[`AltName`](../fontinfo/altname/) (eğer varsa).

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

* class [FontSubstitutionRule](../fontsubstitutionrule/)
* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
