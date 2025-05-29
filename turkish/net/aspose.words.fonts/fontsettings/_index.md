---
title: FontSettings Class
linktitle: FontSettings
articleTitle: FontSettings
second_title: .NET için Aspose.Words
description: Gelişmiş okunabilirlik ve profesyonel sunum için belge yazı tipi ayarlarını zahmetsizce özelleştirmek üzere Aspose.Words.Fonts.FontSettings sınıfını keşfedin.
type: docs
weight: 3400
url: /tr/net/aspose.words.fonts/fontsettings/
---
## FontSettings class

Bir belge için yazı tipi ayarlarını belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yazı Tipleriyle Çalışma](https://docs.aspose.com/words/net/working-with-fonts/) belgeleme makalesi.

```csharp
public class FontSettings
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FontSettings](fontsettings/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| static [DefaultInstance](../../aspose.words.fonts/fontsettings/defaultinstance/) { get; } | Statik varsayılan yazı tipi ayarları. |
| [FallbackSettings](../../aspose.words.fonts/fontsettings/fallbacksettings/) { get; } | Yazı tipi geri dönüş mekanizmasıyla ilgili ayarlar. |
| [SubstitutionSettings](../../aspose.words.fonts/fontsettings/substitutionsettings/) { get; } | Font değiştirme mekanizmasıyla ilgili ayarlar. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetFontsSources](../../aspose.words.fonts/fontsettings/getfontssources/)() | Aspose.Words'ün TrueType yazı tiplerini aradığı kaynakların listesini içeren dizinin bir kopyasını alır. |
| [ResetFontSources](../../aspose.words.fonts/fontsettings/resetfontsources/)() | Yazı tipi kaynaklarını sistem varsayılanına sıfırlar. |
| [SaveSearchCache](../../aspose.words.fonts/fontsettings/savesearchcache/)(*Stream*) | Yazı tipi arama önbelleğini akışa kaydeder. |
| [SetFontsFolder](../../aspose.words.fonts/fontsettings/setfontsfolder/)(*string, bool*) | Aspose.Words'ün belgeleri işlerken veya yazı tiplerini yerleştirirken TrueType yazı tiplerini aradığı klasörü ayarlar. Bu,[`SetFontsFolders`](./setfontsfolders/) sadece bir font dizini ayarlamak için. |
| [SetFontsFolders](../../aspose.words.fonts/fontsettings/setfontsfolders/)(*string[], bool*) | Aspose.Words'ün belgeleri işlerken veya yazı tiplerini yerleştirirken TrueType yazı tiplerini arayacağı klasörleri ayarlar. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources)(*FontSourceBase[]*) | Aspose.Words'ün belgeleri işlerken veya yazı tiplerini yerleştirirken TrueType yazı tiplerini aradığı kaynakları ayarlar. |
| [SetFontsSources](../../aspose.words.fonts/fontsettings/setfontssources/#setfontssources_1)(*FontSourceBase[], Stream*) | Aspose.Words'ün TrueType yazı tiplerini aradığı kaynakları ayarlar ve ayrıca daha önce kaydedilmiş yazı tipi arama önbelleğini yükler. |

## Notlar

Aspose.Words, belgedeki yazı tiplerini çözümlemek için yazı tipi ayarlarını kullanır. Yazı tipleri çoğunlukla belge layout oluştururken veya sabit sayfa biçimlerine işlerken çözümlenir. Ancak bazı biçimleri yüklerken Aspose.Words yazı tiplerini çözümlemeyi de gerektirebilir. Örneğin, when HTML belgeleri yüklerken Aspose.Words yazı tipi geri dönüşünü gerçekleştirmek için yazı tiplerini çözümleyebilir. Bu nedenle yazı tipi ayarlarını içinde ayarlamanız önerilir[`LoadOptions`](../../aspose.words.loading/loadoptions/) belgeyi yüklerken. Ya da en azından düzeni oluşturmadan veya belgeyi sabit sayfa biçimine dönüştürmeden önce.

Varsayılan olarak tüm belgeler tek statik yazı tipi ayarları örneğini kullanır. Buna tarafından erişilebilir.[`DefaultInstance`](./defaultinstance/) mülk.

Yazı tipi ayarlarını değiştirmek her zaman her iş parçacığından güvenlidir. Ancak bu ayarları kullanan bazı belgeleri işlerken yazı tipi ayarlarını değiştirmemeniz önerilir. Bu, aynı yazı tipinin belgenin farklı bölümlerinde farklı şekilde çözülmesine yol açabilir.

## Örnekler

Mevcut font kaynaklarımıza nasıl font kaynağı ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arial";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);

Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Varsayılan yazı tipi kaynağında, belgemizde kullandığımız iki yazı tipi eksik.
// Bu belgeyi kaydettiğimizde, Aspose.Words erişilemeyen yazı tipleriyle biçimlendirilmiş tüm metinlere yedek yazı tiplerini uygulayacaktır.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// Fontları içeren bir klasörden bir font kaynağı oluştur.
FolderFontSource folderFontSource = new FolderFontSource(FontsDir, true);

// Orijinal yazı tipi kaynaklarının yanı sıra özel yazı tiplerimizi de içeren yeni bir yazı tipi kaynakları dizisi uygulayın.
FontSourceBase[] updatedFontSources = {originalFontSources[0], folderFontSource};
FontSettings.DefaultInstance.SetFontsSources(updatedFontSources);

// Belgeyi PDF'e dönüştürmeden önce Aspose.Words'ün tüm gerekli yazı tiplerine erişiminin olduğunu doğrulayın.
updatedFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.True(updatedFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.True(updatedFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

doc.Save(ArtifactsDir + "FontSettings.AddFontSource.pdf");

// Orijinal yazı tipi kaynaklarını geri yükleyin.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Yazı tipi kaynak dizininin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Arvo";
builder.Writeln("Hello world!");
builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Yazı tipi kaynaklarımız bu belgede metin için kullandığımız yazı tipini içermiyor.
// Bu dokümanı oluştururken bu yazı tipi ayarlarını kullanırsak,
// Aspose.Words, Aspose.Words'ün bulamadığı bir yazı tipine sahip metne yedek bir yazı tipi uygulayacaktır.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Varsayılan yazı tipi kaynaklarında bu belgede kullandığımız iki yazı tipi eksik.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// Yeni bir font kaynağı olarak işlev görecek bir dizin ayarlamak için "SetFontsFolder" yöntemini kullanın.
// Dizin içindeki tüm yazı tipi dosyalarındaki yazı tiplerini dahil etmek için "yinelemeli" argüman olarak "false" değerini geçirin
// ilk argümanı geçiriyoruz ancak o dizinin alt klasörlerindeki hiçbir yazı tipini dahil etmiyoruz.
// Dizinimizde bulunan tüm yazı tipi dosyalarını dahil etmek için "tekrarlı" argüman olarak "true" değerini geçirin
// ilk argümanda ve alt dizinlerindeki tüm fontlarda.
FontSettings.DefaultInstance.SetFontsFolder(FontsDir, recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arvo"));

// "Amethysta" yazı tipi font dizininin bir alt klasöründedir.
if (recursive)
{
    Assert.AreEqual(25, newFontSources[0].GetAvailableFonts().Count);
    Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}
else
{
    Assert.AreEqual(18, newFontSources[0].GetAvailableFonts().Count);
    Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolder.pdf");

// Orijinal yazı tipi kaynaklarını geri yükleyin.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

Birden fazla font kaynak dizininin nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Font.Name = "Amethysta";
builder.Writeln("The quick brown fox jumps over the lazy dog.");
builder.Font.Name = "Junction Light";
builder.Writeln("The quick brown fox jumps over the lazy dog.");

// Yazı tipi kaynaklarımız bu belgede metin için kullandığımız yazı tipini içermiyor.
// Bu dokümanı oluştururken bu yazı tipi ayarlarını kullanırsak,
// Aspose.Words, Aspose.Words'ün bulamadığı bir yazı tipine sahip metne yedek bir yazı tipi uygulayacaktır.
FontSourceBase[] originalFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(1, originalFontSources.Length);
Assert.True(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));

// Varsayılan yazı tipi kaynaklarında bu belgede kullandığımız iki yazı tipi eksik.
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));
Assert.False(originalFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));

// İlk argüman olarak geçirdiğimiz her font dizininden bir font kaynağı oluşturmak için "SetFontsFolders" metodunu kullanın.
// Dizinlerdeki tüm yazı tipi dosyalarındaki yazı tiplerini dahil etmek için "yinelemeli" argüman olarak "false" değerini geçirin
// ilk argümanı geçiriyoruz ancak dizinlerin alt klasörlerinden hiçbir fontu dahil etmiyoruz.
// Geçirdiğimiz dizinlerdeki tüm yazı tipi dosyalarını dahil etmek için "tekrarlı" argüman olarak "true" değerini geçirin
// ilk argümanda ve alt dizinlerindeki tüm fontlarda.
FontSettings.DefaultInstance.SetFontsFolders(new[] {FontsDir + "/Amethysta", FontsDir + "/Junction"},
    recursive);

FontSourceBase[] newFontSources = FontSettings.DefaultInstance.GetFontsSources();

Assert.AreEqual(2, newFontSources.Length);
Assert.False(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Arial"));
Assert.AreEqual(1, newFontSources[0].GetAvailableFonts().Count);
Assert.True(newFontSources[0].GetAvailableFonts().Any(f => f.FullFontName == "Amethysta"));

// "Junction" klasörünün kendisi herhangi bir font dosyası içermez, ancak bunu yapan alt klasörlere sahiptir.
if (recursive)
{
    Assert.AreEqual(6, newFontSources[1].GetAvailableFonts().Count);
    Assert.True(newFontSources[1].GetAvailableFonts().Any(f => f.FullFontName == "Junction Light"));
}
else
{
    Assert.AreEqual(0, newFontSources[1].GetAvailableFonts().Count);
}

doc.Save(ArtifactsDir + "FontSettings.SetFontsFolders.pdf");

// Orijinal yazı tipi kaynaklarını geri yükleyin.
FontSettings.DefaultInstance.SetFontsSources(originalFontSources);
```

### Ayrıca bakınız

* ad alanı [Aspose.Words.Fonts](../../aspose.words.fonts/)
* toplantı [Aspose.Words](../../)
