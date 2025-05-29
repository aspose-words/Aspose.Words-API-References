---
title: Hyphenation.RegisterDictionary
linktitle: RegisterDictionary
articleTitle: RegisterDictionary
second_title: .NET için Aspose.Words
description: Hyphenation RegisterDictionary yöntemiyle metin işlemeyi zahmetsizce geliştirin. En iyi sonuçlar için dil özelinde tireleme sözlüklerini sorunsuz bir şekilde yükleyin.
type: docs
weight: 40
url: /tr/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(*string, Stream*) {#registerdictionary}

Belirtilen dil için bir tireleme sözlüğünü bir akıştan kaydeder ve yükler. Sözlük okunamıyorsa veya geçersiz biçime sahipse fırlatır.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| language | String | Bir dil adı, örneğin "en-US". "Kültür adı" için .NET belgelerine ve ayrıntılar için RFC 4646'ya bakın. |
| stream | Stream | OpenOffice formatındaki sözlük dosyası için bir akış. |

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

* class [Hyphenation](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## RegisterDictionary(*string, string*) {#registerdictionary_1}

Belirtilen dil için bir tireleme sözlüğünü dosyadan kaydeder ve yükler. Sözlük okunamıyorsa veya geçersiz bir biçime sahipse fırlatır.

Bu yöntem, Null sözlüğünü kaydetmek için de kullanılabilir.[`Callback`](../callback/) aynı dil için tekrar tekrar çağrılmaktan.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| language | String | Bir dil adı, örneğin "en-US". "Kültür adı" için .NET belgelerine ve ayrıntılar için RFC 4646'ya bakın. |
| fileName | String | Open Office formatındaki sözlük dosyasına giden yol. |

## Örnekler

Bir tireleme sözlüğünün nasıl kaydedileceğini gösterir.

```csharp
// Bir tireleme sözlüğü, sözlüğün dili için tireleme kurallarını tanımlayan dizelerin bir listesini içerir.
// Bir belge, bir kelimenin bölünebileceği ve bir sonraki satırda devam ettirilebileceği metin satırları içeriyorsa,
// tireleme, sözlüğün dize listesinde o kelimenin alt dizelerini arayacaktır.
// Eğer sözlük bir alt dize içeriyorsa, tireleme kelimeyi iki satıra böler
// alt dizeye göre ve ilk yarıya bir tire ekleyin.
// Yerel dosya sisteminden "de-CH" yereline bir sözlük dosyası kaydedin.
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Sözlüğümüzle eşleşen bir yerel ayara sahip metin içeren bir belge açın,
// ve sabit sayfa kaydetme biçimine kaydedin. Bu belgedeki metin tireli olacaktır.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Sözlüğün kaydı silindikten sonra belgeyi yeniden yükleyin,
// ve tireli metin içermeyen başka bir PDF'ye kaydedin.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

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

* class [Hyphenation](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
