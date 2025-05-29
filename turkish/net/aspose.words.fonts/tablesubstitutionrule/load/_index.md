---
title: TableSubstitutionRule.Load
linktitle: Load
articleTitle: Load
second_title: .NET için Aspose.Words
description: TableSubstitutionRule Load yöntemi ile XML dosyalarından tablo değiştirme ayarlarını zahmetsizce yükleyin. Veri yönetiminizi bugün optimize edin!
type: docs
weight: 30
url: /tr/net/aspose.words.fonts/tablesubstitutionrule/load/
---
## Load(*string*) {#load_1}

XML dosyasından tablo değiştirme ayarlarını yükler.

```csharp
public void Load(string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| fileName | String | Dosya adını girin. |

## Örnekler

Özel yazı tipi değiştirme tablolarıyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Yeni bir tablo değiştirme kuralı oluştur ve varsayılan Windows yazı tipi değiştirme tablosunu yükle.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Eğer sadece klasörümüzden font seçersek, özel bir ikame tablosuna ihtiyacımız olacak.
// Artık Microsoft Windows yazı tiplerine erişimimiz olmayacak,
// "Arial" veya "Times New Roman" gibi fontlar yeni font klasörümüzde bulunmadığından.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Aşağıda yerel dosya sistemindeki bir dosyadan bir ikame tablosunu yüklemenin iki yolu bulunmaktadır.
// 1 - Bir akıştan:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Doğrudan bir dosyadan:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Artık "Arial"a erişimimiz olmadığından, yazı tipi tablomuz ilk önce onu "Varolan Yazı Tipi" ile değiştirmeyi deneyecektir.
// Bu yazı tipine sahip olmadığımızdan, "MyFonts" klasöründe bulunan bir sonraki yedek olan "Kreon"a taşınacaktır.
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Bu tabloyu programatik olarak genişletebiliriz. "Times New Roman" yerine "Arvo" koyan bir giriş ekleyeceğiz
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// AddSubstitutes() ile mevcut bir yazı tipi girişi için ikincil bir yedek ekleyebiliriz.
// "Arvo" mevcut değilse, tablomuz ikinci ikame seçeneği olarak "M+ 2m"yi arayacaktır.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() bir yazı tipi için yeni bir yedek yazı tipi listesi ayarlayabilir.
tableSubstitutionRule.SetSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Erişimimizin olmadığı yazı tiplerinde metin yazmak, ikame kurallarımızı devreye sokacaktır.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Ayrıca bakınız

* class [TableSubstitutionRule](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)

---

## Load(*Stream*) {#load}

XML akışından tablo değiştirme ayarlarını yükler.

```csharp
public void Load(Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| stream | Stream | Giriş akışı. |

## Örnekler

Özel yazı tipi değiştirme tablolarıyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Yeni bir tablo değiştirme kuralı oluştur ve varsayılan Windows yazı tipi değiştirme tablosunu yükle.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Eğer sadece klasörümüzden font seçersek, özel bir ikame tablosuna ihtiyacımız olacak.
// Artık Microsoft Windows yazı tiplerine erişimimiz olmayacak,
// "Arial" veya "Times New Roman" gibi fontlar yeni font klasörümüzde bulunmadığından.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Aşağıda yerel dosya sistemindeki bir dosyadan bir ikame tablosunu yüklemenin iki yolu bulunmaktadır.
// 1 - Bir akıştan:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Doğrudan bir dosyadan:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Artık "Arial"a erişimimiz olmadığından, yazı tipi tablomuz ilk önce onu "Varolan Yazı Tipi" ile değiştirmeyi deneyecektir.
// Bu yazı tipine sahip olmadığımızdan, "MyFonts" klasöründe bulunan bir sonraki yedek olan "Kreon"a taşınacaktır.
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Bu tabloyu programatik olarak genişletebiliriz. "Times New Roman" yerine "Arvo" koyan bir giriş ekleyeceğiz
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// AddSubstitutes() ile mevcut bir yazı tipi girişi için ikincil bir yedek ekleyebiliriz.
// "Arvo" mevcut değilse, tablomuz ikinci ikame seçeneği olarak "M+ 2m"yi arayacaktır.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes() bir yazı tipi için yeni bir yedek yazı tipi listesi ayarlayabilir.
tableSubstitutionRule.SetSubstitutes("Times New Roman", "Squarish Sans CT", "M+ 2m");
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Erişimimizin olmadığı yazı tiplerinde metin yazmak, ikame kurallarımızı devreye sokacaktır.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Font.Name = "Arial";
builder.Writeln("Text written in Arial, to be substituted by Kreon.");

builder.Font.Name = "Times New Roman";
builder.Writeln("Text written in Times New Roman, to be substituted by Squarish Sans CT.");

doc.Save(ArtifactsDir + "FontSettings.TableSubstitutionRule.Custom.pdf");
```

### Ayrıca bakınız

* class [TableSubstitutionRule](../)
* ad alanı [Aspose.Words.Fonts](../../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../../)
