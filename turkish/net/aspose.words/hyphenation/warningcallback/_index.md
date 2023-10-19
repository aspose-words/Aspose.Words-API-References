---
title: Hyphenation.WarningCallback
linktitle: WarningCallback
articleTitle: WarningCallback
second_title: Aspose.Words for .NET
description: Hyphenation WarningCallback mülk. Yük tireleme desenleri sırasında biçimlendirme aslına uygunluk kaybına yol açabilecek bir sorun algılandığında çağrılır C#'da.
type: docs
weight: 20
url: /tr/net/aspose.words/hyphenation/warningcallback/
---
## Hyphenation.WarningCallback property

Yük tireleme desenleri sırasında, biçimlendirme aslına uygunluk kaybına yol açabilecek bir sorun algılandığında çağrılır.

```csharp
public static IWarningCallback WarningCallback { get; set; }
```

## Örnekler

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

* interface [IWarningCallback](../../iwarningcallback/)
* class [Hyphenation](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
