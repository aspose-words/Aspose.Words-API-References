---
title: Hyphenation Class
linktitle: Hyphenation
articleTitle: Hyphenation
second_title: .NET için Aspose.Words
description: Etkili tireleme yönetimi için Aspose.Words.Hyphenation sınıfını keşfedin. Belgelerinizi kesin dil-özel tireleme kurallarıyla geliştirin.
type: docs
weight: 3580
url: /tr/net/aspose.words/hyphenation/
---
## Hyphenation class

Tireleme sözlükleriyle çalışmak için yöntemler sağlar. Bu sözlükler belirli bir dilin kelimelerinin nerede tirelenebileceğini belirtir.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Tireleme ile Çalışma](https://docs.aspose.com/words/net/working-with-hyphenation/) belgeleme makalesi.

```csharp
public static class Hyphenation
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| static [Callback](../../aspose.words/hyphenation/callback/) { get; set; } | Belgenin sayfa düzeni oluşturulurken sözlükleri istemek için kullanılan geri çağırma arayüzünü alır veya ayarlar. Bu, birçok dildeki belgeleri işlerken yararlı olabilecek sözlüklerin gecikmeli yüklenmesine izin verir. |
| static [WarningCallback](../../aspose.words/hyphenation/warningcallback/) { get; set; } | Biçimlendirme sadakat kaybına yol açabilecek bir sorun algılandığında, yükleme tireleme desenleri sırasında çağrılır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| static [IsDictionaryRegistered](../../aspose.words/hyphenation/isdictionaryregistered/)(*string*) | Geri Döndürür`YANLIŞ` Belirtilen dil için kayıtlı bir sözlük yoksa veya kayıtlı sözlük Null ise,`doğru` aksi takdirde. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary)(*string, Stream*) | Belirtilen dil için bir tireleme sözlüğünü bir akıştan kaydeder ve yükler. Sözlük okunamıyorsa veya geçersiz biçime sahipse fırlatır. |
| static [RegisterDictionary](../../aspose.words/hyphenation/registerdictionary/#registerdictionary_1)(*string, string*) | Belirtilen dil için bir tireleme sözlüğünü dosyadan kaydeder ve yükler. Sözlük okunamıyorsa veya geçersiz bir biçime sahipse fırlatır. |
| static [UnregisterDictionary](../../aspose.words/hyphenation/unregisterdictionary/)(*string*) | Belirtilen dil için bir tireleme sözlüğünün kaydını siler. |

## Örnekler

Bir sözlüğün dosyadan nasıl açılıp kaydedileceğini gösterir.

```csharp
public void RegisterDictionary()
{
    // Heceleme sözlüğü kaydı sırasında oluşan uyarıları izleyen bir geri arama ayarlayın.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Akış yoluyla bir İngilizce (ABD) tireleme sözlüğü kaydedin.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Microsoft Word'ün İngilizce bir bilgisayarda tireleyemeyeceği bir yerel ayara sahip bir belgeyi (örneğin Almanca) açın.
    Document doc = new Document(MyDir + "German text.docx");

    // Bu belgeyi kaydederken tirelemek için, "de-CH" dil koduna yönelik bir tireleme sözlüğüne ihtiyacımız var.
    // Bu geri çağırma, söz konusu sözlük için otomatik isteği işleyecektir.
    Hyphenation.Callback = new CustomHyphenationDictionaryRegister();

    // Belgeyi kaydettiğimizde Almanca tireleme devreye girecek.
    doc.Save(ArtifactsDir + "Hyphenation.RegisterDictionary.pdf");

    // Bu sözlük, bir uyarıyı tetikleyecek iki özdeş desen içeriyor.
    Assert.AreEqual(1, warningInfoCollection.Count);
    Assert.AreEqual(WarningType.MinorFormattingLoss, warningInfoCollection[0].WarningType);
    Assert.AreEqual(WarningSource.Layout, warningInfoCollection[0].Source);
    Assert.AreEqual("Hyphenation dictionary contains duplicate patterns. The only first found pattern will be used. " +
                    "Content can be wrapped differently.", warningInfoCollection[0].Description);

}

/// <summary>
/// ISO dil kodlarını tireleme sözlüğü dosyaları için yerel sistem dosya adlarıyla ilişkilendirir.
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
