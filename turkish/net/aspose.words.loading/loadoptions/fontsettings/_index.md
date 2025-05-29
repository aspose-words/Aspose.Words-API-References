---
title: LoadOptions.FontSettings
linktitle: FontSettings
articleTitle: FontSettings
second_title: .NET için Aspose.Words
description: Gelişmiş okunabilirlik ve stil için belgenizin yazı tipi ayarlarını LoadOptions FontSettings ile özelleştirin. Belgelerinizi zahmetsizce optimize edin!
type: docs
weight: 60
url: /tr/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

Belge yazı tipi ayarlarının belirlenmesine olanak tanır.

```csharp
public FontSettings FontSettings { get; set; }
```

## Notlar

Bazı biçimleri yüklerken, Aspose.Words yazı tiplerini çözümlemeyi gerektirebilir. Örneğin, HTML belgelerini yüklerken Aspose.Words yazı tipi geri dönüşünü gerçekleştirmek için yazı tiplerini çözümleyebilir.

Eğer ayarlanırsa`hükümsüz` , varsayılan statik yazı tipi ayarları[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) kullanılacaktır.

Varsayılan değer:`hükümsüz`.

## Örnekler

Bir belge yüklenirken yazı tipi değiştirme ayarlarının nasıl uygulanacağını gösterir.

```csharp
// "Times New Roman" yazı tipini değiştirecek bir FontSettings nesnesi oluşturun
// "MyFonts" klasörümüzdeki "Arvo" fontuyla.
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// FontSettings nesnesini yeni oluşturulan LoadOptions nesnesinin bir özelliği olarak ayarlayın.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// Belgeyi yükleyin, ardından yazı tipini değiştirerek PDF olarak işleyin.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

Yükleme sırasında yazı tipi ikamelerinin nasıl belirleneceğini gösterir.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// LoadOptions nesnesi için bir yazı tipi değiştirme kuralı ayarlayın.
// Yüklediğimiz belge sahip olmadığımız bir yazı tipini kullanıyorsa,
// bu kural mevcut olmayan yazı tipini mevcut olanla değiştirecektir.
// Bu durumda "MissingFont"un tüm kullanımları "Comic Sans MS"e dönüşecektir.
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", "Comic Sans MS");

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// Bu noktada söz konusu metin hala "MissingFont" içinde olacaktır.
// Yazı tipi değişimi belgeyi render ettiğimizde gerçekleşecek.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### Ayrıca bakınız

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../../aspose.words.loading/)
* toplantı [Aspose.Words](../../../)
