---
title: LoadOptions.FontSettings
second_title: Aspose.Words for .NET API Referansı
description: LoadOptions mülk. Belge yazı tipi ayarlarını belirlemeye izin verir.
type: docs
weight: 60
url: /tr/net/aspose.words.loading/loadoptions/fontsettings/
---
## LoadOptions.FontSettings property

Belge yazı tipi ayarlarını belirlemeye izin verir.

```csharp
public FontSettings FontSettings { get; set; }
```

### Notlar

Bazı formatları yüklerken Aspose.Words'ün yazı tiplerini çözmesi gerekebilir. Örneğin, HTML belgeleri yüklenirken Aspose.Words , yazı tipi geri dönüşünü gerçekleştirmek için yazı tiplerini çözebilir.

Eğer ayarlanmışsa`hükümsüz` , varsayılan statik yazı tipi ayarları[`DefaultInstance`](../../../aspose.words.fonts/fontsettings/defaultinstance/) kullanılacak.

Varsayılan değer:`hükümsüz`.

### Örnekler

Bir belge yüklenirken yazı tipi değiştirme ayarlarının nasıl uygulanacağını gösterir.

```csharp
// "Times New Roman" yazı tipinin yerini alacak bir FontSettings nesnesi oluşturun
// "MyFonts" klasörümüzden "Arvo" yazı tipiyle.
FontSettings fontSettings = new FontSettings();
fontSettings.SetFontsFolder(FontsDir, false);
fontSettings.SubstitutionSettings.TableSubstitution.AddSubstitutes("Times New Roman", "Arvo");

// FontSettings nesnesini yeni oluşturulan LoadOptions nesnesinin bir özelliği olarak ayarlayın.
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = fontSettings;

// Belgeyi yükleyin, ardından yazı tipi değişikliğiyle PDF olarak dönüştürün.
Document doc = new Document(MyDir + "Document.docx", loadOptions);

doc.Save(ArtifactsDir + "LoadOptions.FontSettings.pdf");
```

Yükleme sırasında yazı tipi yedeklerinin nasıl belirleneceğini gösterir.

```csharp
LoadOptions loadOptions = new LoadOptions();
loadOptions.FontSettings = new FontSettings();

// LoadOptions nesnesi için yazı tipi değiştirme kuralını ayarlayın.
// Yüklediğimiz belge bizde olmayan bir font kullanıyorsa,
// bu kural, kullanılamayan yazı tipini mevcut olanla değiştirecektir.
// Bu durumda, "MissingFont"un tüm kullanımları "Comic Sans MS"e dönüştürülecektir.
TableSubstitutionRule substitutionRule = loadOptions.FontSettings.SubstitutionSettings.TableSubstitution;
substitutionRule.AddSubstitutes("MissingFont", new[] {"Comic Sans MS"});

Document doc = new Document(MyDir + "Missing font.html", loadOptions);

// Bu noktada bu tür metinler hâlâ "MissingFont"ta olacaktır.
// Belgeyi oluşturduğumuzda yazı tipi değişikliği gerçekleşecek.
Assert.AreEqual("MissingFont", doc.FirstSection.Body.FirstParagraph.Runs[0].Font.Name);

doc.Save(ArtifactsDir + "FontSettings.ResolveFontsBeforeLoadingDocument.pdf");
```

### Ayrıca bakınız

* class [FontSettings](../../../aspose.words.fonts/fontsettings/)
* class [LoadOptions](../)
* ad alanı [Aspose.Words.Loading](../../loadoptions/)
* toplantı [Aspose.Words](../../../)


