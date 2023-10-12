---
title: Class Hyphenation
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Hyphenation sınıf. Tireleme sözlükleriyle çalışmaya yönelik yöntemler sağlar. Bu sözlükler belirli bir dildeki kelimelerin nerede tirelenebileceğini belirler.
type: docs
weight: 3150
url: /tr/net/aspose.words/hyphenation/
---
## Hyphenation class

Tireleme sözlükleriyle çalışmaya yönelik yöntemler sağlar. Bu sözlükler, belirli bir dildeki kelimelerin nerede tirelenebileceğini belirler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Tireleme ile Çalışmak](https://docs.aspose.com/words/net/working-with-hyphenation/) dokümantasyon makalesi.

```csharp
public static class Hyphenation
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Belgenin sayfa düzeni oluşturulduğunda sözlük istemek için kullanılan geri arama arayüzünü alır veya ayarlar. Bu, birçok dilde belgeler işlenirken faydalı olabilecek sözlüklerin gecikmeli yüklenmesine olanak tanır. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Yük tireleme desenleri sırasında, biçimlendirme aslına uygunluk kaybına yol açabilecek bir sorun algılandığında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(string) | İadeler`YANLIŞ` belirtilen dil için kayıtlı sözlük yoksa veya kayıtlıysa Boş sözlük ise,`doğru` aksi halde. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(string, Stream) | Bir akıştan belirtilen dil için bir tireleme sözlüğünü kaydeder ve yükler. Sözlüğün okunamaması veya biçiminin geçersiz olması durumunda hata oluşur. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(string, string) | Dosyadan belirtilen dil için bir tireleme sözlüğünü kaydeder ve yükler. Sözlüğün okunamaması veya biçiminin geçersiz olması durumunda hata oluşur. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(string) | Belirtilen dil için tireleme sözlüğünün kaydını siler. |

### Örnekler

Bir dosyadan sözlüğün nasıl açılacağını ve kaydedileceğini gösterir.

```csharp
public void RegisterDictionary()
{
    // Tireleme sözlüğü kaydı sırasında oluşan uyarıları izleyen bir geri arama ayarlayın.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Akışa göre bir İngilizce (ABD) tireleme sözlüğü kaydedin.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Almanca gibi İngilizce bir makinede Microsoft Word'ün tireleme yapamayacağı bir yerel ayara sahip bir belge açın.
    Document doc = new Document(MyDir + "German text.docx");

    // Bu belgeyi kaydettikten sonra tirelemek için, "de-CH" dil koduna yönelik bir tireleme sözlüğüne ihtiyacımız var.
    // Bu geri çağırma söz konusu sözlük için otomatik isteği yerine getirecektir.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Belgeyi kaydettiğimizde Almanca tireleme geçerli olacaktır.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Bu sözlük, bir uyarıyı tetikleyecek iki özdeş kalıp içerir.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);
}

/// <summary>
/// Tireleme sözlük dosyaları için ISO dil kodlarını yerel sistem dosya adlarıyla ilişkilendirir.
/// </summary>
private class CustomHyphenationDictionaryRegister : IHyphenationCallback
{
    public CustomHyphenationDictionaryRegister()
    {
        mHyphenationDictionaryFiles = new Dictionary<string, string>
        {
            { "en-US", MyDir + "hyph_en_US.dic" },
            { "de-CH", MyDir + "hyph_de_CH.dic" }
        };
    }

    public void RequestDictionary(string language)
    {
        Console.Write("Hyphenation dictionary requested: " + language);

        if (Hyphenation.IsDictionaryRegistered(language))
        {
            Console.WriteLine(", is already registered.");
            return;
        }

        if (mHyphenationDictionaryFiles.ContainsKey(language))
        {
            Hyphenation.RegisterDictionary(language, mHyphenationDictionaryFiles[language]);
            Console.WriteLine(", successfully registered.");
            return;
        }

        Console.WriteLine(", no respective dictionary file known by this Callback.");
    }

    private readonly Dictionary<string, string> mHyphenationDictionaryFiles;
}
```

### Ayrıca bakınız

* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)


