---
title: TableSubstitutionRule.SetSubstitutes
second_title: Aspose.Words for .NET API Referansı
description: TableSubstitutionRule yöntem. Verilen orijinal yazı tipi adı için yedek yazı tipi adlarını geçersiz kıl.
type: docs
weight: 80
url: /tr/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Verilen orijinal yazı tipi adı için yedek yazı tipi adlarını geçersiz kıl.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| originalFontName | String | Orijinal yazı tipi adı. |
| substituteFontNames | String[] | Alternatif yazı tipi adlarının listesi. |

### Örnekler

Yazı tipi değiştirme kurallarının nasıl ayarlandığını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] fontSources = FontSettings.DefaultInstance.GetFontsSources();

// Varsayılan yazı tipi kaynakları, belgenin kullandığı ilk yazı tipini içerir.
Assert.AreEqual(1, fontSources.Length);
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// İkinci yazı tipi olan "Amethysta" kullanılamıyor.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Belirleyen bir yazı tipi değiştirme tablosu yapılandırabiliriz
// Aspose.Words'ün mevcut olmayan yazı tiplerinin yerine hangi yazı tiplerini kullanacağı.
// "Amethysta" için iki ikame yazı tipi ayarlayın: "Arvo" ve "Courier New".
// İlk ikame kullanılamıyorsa Aspose.Words ikinci ikameyi kullanmayı dener ve bu şekilde devam eder.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" kullanılamıyor ve değiştirme kuralı, yerine kullanılacak ilk yazı tipinin "Arvo" olduğunu belirtir.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" da mevcut değil, ancak "Courier New" mevcut.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Çıktı belgesi "Courier New" ile biçimlendirilmiş "Amethysta" yazı tipini kullanan metni görüntüleyecektir.
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

Özel yazı tipi değiştirme tablolarıyla nasıl çalışılacağını gösterir.

```csharp
Document doc = new Document();
FontSettings fontSettings = new FontSettings();
doc.FontSettings = fontSettings;

// Yeni bir tablo değiştirme kuralı oluşturun ve varsayılan Windows yazı tipi değiştirme tablosunu yükleyin.
TableSubstitutionRule tableSubstitutionRule = fontSettings.SubstitutionSettings.TableSubstitution;

// Eğer yazı tiplerini özel olarak klasörümüzden seçersek, özel bir değiştirme tablosuna ihtiyacımız olacak.
// Artık Microsoft Windows yazı tiplerine erişimimiz olmayacak,
// yeni yazı tipi klasörümüzde bulunmadığından "Arial" veya "Times New Roman" gibi.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, false);
fontSettings.SetFontsSources(new FontSourceBase[] {folderFontSource});

// Aşağıda yerel dosya sistemindeki bir dosyadan değiştirme tablosu yüklemenin iki yolu verilmiştir.
// 1 - Bir akıştan:
using (FileStream fileStream = new FileStream(MyDir + "Font substitution rules.xml", FileMode.Open))
{
    tableSubstitutionRule.Load(fileStream);
}

// 2 - Doğrudan bir dosyadan:
tableSubstitutionRule.Load(MyDir + "Font substitution rules.xml");

// Artık "Arial"a erişimimiz olmadığından, yazı tipi tablomuz öncelikle onu "Var Olmayan Yazı Tipi" ile değiştirmeyi deneyecek.
// Bu yazı tipine sahip değiliz, böylece "MyFonts" klasöründe bulunan bir sonraki yedek olan "Kreon"a geçecektir.
Assert.AreEqual(new[] {"Missing Font", "Kreon"}, tableSubstitutionRule.GetSubstitutes("Arial").ToArray());

// Bu tabloyu programlı olarak genişletebiliriz. "Times New Roman" yerine "Arvo" yazan bir giriş ekleyeceğiz
Assert.Null(tableSubstitutionRule.GetSubstitutes("Times New Roman"));
tableSubstitutionRule.AddSubstitutes("Times New Roman", "Arvo");
Assert.AreEqual(new[] {"Arvo"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// AddSubstitutes() ile mevcut bir yazı tipi girişinin yerine ikincil bir yedek yedek ekleyebiliriz.
// "Arvo"nun mevcut olmaması durumunda tablomuz ikinci yedek seçenek olarak "M+ 2m"yi arayacaktır.
tableSubstitutionRule.AddSubstitutes("Times New Roman", "M+ 2m");
Assert.AreEqual(new[] {"Arvo", "M+ 2m"}, tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// SetSubstitutes(), bir yazı tipi için yeni bir yedek yazı tipi listesi ayarlayabilir.
tableSubstitutionRule.SetSubstitutes("Times New Roman", new[] {"Squarish Sans CT", "M+ 2m"});
Assert.AreEqual(new[] {"Squarish Sans CT", "M+ 2m"},
    tableSubstitutionRule.GetSubstitutes("Times New Roman").ToArray());

// Erişemediğimiz yazı tipleriyle metin yazmak, değiştirme kurallarımızı devreye sokacaktır.
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


