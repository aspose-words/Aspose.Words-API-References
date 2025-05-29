---
title: TableSubstitutionRule.SetSubstitutes
linktitle: SetSubstitutes
articleTitle: SetSubstitutes
second_title: .NET için Aspose.Words
description: TableSubstitutionRule SetSubstitutes yöntemi ile yazı tipi adlarını nasıl özelleştireceğinizi keşfedin. Tasarımınızı özel tipografi çözümleriyle geliştirin!
type: docs
weight: 80
url: /tr/net/aspose.words.fonts/tablesubstitutionrule/setsubstitutes/
---
## TableSubstitutionRule.SetSubstitutes method

Belirtilen orijinal yazı tipi adı için yedek yazı tipi adlarını geçersiz kıl.

```csharp
public void SetSubstitutes(string originalFontName, params string[] substituteFontNames)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| originalFontName | String | Orijinal yazı tipi adı. |
| substituteFontNames | String[] | Alternatif font adlarının listesi. |

## Örnekler

Yazı tipi değiştirme kurallarının nasıl ayarlanacağını gösterir.

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

// İkinci font olan "Amethysta" mevcut değil.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Aşağıdakileri belirleyen bir yazı tipi değiştirme tablosu yapılandırabiliriz:
// Aspose.Words'ün kullanılamayan yazı tiplerinin yerine hangi yazı tiplerini kullanacağı.
// "Amethysta" için iki yedek yazı tipi ayarlayın: "Arvo" ve "Courier New".
// Eğer ilk ikame mevcut değilse, Aspose.Words ikinci ikameyi kullanmayı dener, vb.
doc.FontSettings = new FontSettings();
doc.FontSettings.SubstitutionSettings.TableSubstitution.SetSubstitutes(
    "Amethysta", new[] {"Arvo", "Courier New"});

 // "Amethysta" mevcut değil ve ikame kuralı, ikame olarak kullanılacak ilk fontun "Arvo" olduğunu belirtiyor.
Assert.False(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

 // "Arvo" da mevcut değil, ancak "Courier New" mevcut.
Assert.True(fontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Courier New"));

// Çıktı belgesinde "Amethysta" yazı tipini kullanan metin "Courier New" ile biçimlendirilmiş olarak görüntülenecektir.
doc.Save(ArtifactsDir + "FontSettings.TableSubstitution.pdf");
```

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
