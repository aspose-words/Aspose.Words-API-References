---
title: Interface IHyphenationCallback
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.IHyphenationCallback arayüz. Tireleme sözlüklerini kaydedebilen sınıflar tarafından uygulanır.
type: docs
weight: 2990
url: /tr/net/aspose.words/ihyphenationcallback/
---
## IHyphenationCallback interface

Tireleme sözlüklerini kaydedebilen sınıflar tarafından uygulanır.

```csharp
public interface IHyphenationCallback
```

## yöntemler

| İsim | Tanım |
| --- | --- |
| [RequestDictionary](../../aspose.words/ihyphenationcallback/requestdictionary/)(string) | Belirtilen dil için tireleme sözlüğünün bulunamadığını ve kaydedilmesi gerekebileceğini uygulamaya bildirir. |

### Örnekler

Bir dosyadan bir sözlüğün nasıl açılacağını ve kaydedileceğini gösterir.

```csharp
{
    // Tireleme sözlüğü kaydı sırasında oluşan uyarıları izleyen bir geri arama ayarlayın.
    WarningInfoCollection warningInfoCollection = new WarningInfoCollection();
    Hyphenation.WarningCallback = warningInfoCollection;

    // Akışa göre bir İngilizce (ABD) tireleme sözlüğü kaydedin.
    Stream dictionaryStream = new FileStream(MyDir + "hyph_en_US.dic", FileMode.Open);
    Hyphenation.RegisterDictionary("en-US", dictionaryStream);

    Assert.AreEqual(0, warningInfoCollection.Count);

    // Almanca gibi bir İngilizce makinede Microsoft Word'ün tireleyemeyeceği bir yerel ayara sahip bir belge açın.
    Document doc = new Document(MyDir + "German text.docx");

    // Bu belgeyi kaydettikten sonra tirelemek için "de-CH" dil kodu için bir tireleme sözlüğüne ihtiyacımız var.
    // Bu geri arama, o sözlük için otomatik isteği işleyecektir.
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
/// Tireleme sözlüğü dosyaları için ISO dil kodlarını yerel sistem dosya adlarıyla ilişkilendirir.
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


