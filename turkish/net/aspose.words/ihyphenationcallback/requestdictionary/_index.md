---
title: IHyphenationCallback.RequestDictionary
linktitle: RequestDictionary
articleTitle: RequestDictionary
second_title: .NET için Aspose.Words
description: IHyphenationCallback RequestDictionary metodunu keşfedin, uygulamanızda kusursuz dil desteği için eksik tireleme sözlüklerini etkin bir şekilde işleyin.
type: docs
weight: 10
url: /tr/net/aspose.words/ihyphenationcallback/requestdictionary/
---
## IHyphenationCallback.RequestDictionary method

Belirtilen dil için tireleme sözlüğünün bulunmadığını ve kaydedilmesi gerekebileceğini uygulamaya bildirir.

Uygulama bir sözlük bulmalı ve onu kullanarak kaydetmelidir[`RegisterDictionary`](../../hyphenation/registerdictionary/) Yöntemler.

Belirtilen dil uygulaması için sözlük mevcut değilse, aynı dil için daha fazla çağrı yapılmayabilir [`RegisterDictionary`](../../hyphenation/registerdictionary/) ile`hükümsüz` değer.

```csharp
public void RequestDictionary(string language)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| language | String | Bir dil adı, örneğin "en-US". "Kültür adı" için .NET belgelerine ve ayrıntılar için RFC 4646'ya bakın. |

## Notlar

Bu yöntem tarafından oluşturulan istisnalar sayfa düzeni işleminin yürütülmesini sonlandıracaktır.

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

* interface [IHyphenationCallback](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
