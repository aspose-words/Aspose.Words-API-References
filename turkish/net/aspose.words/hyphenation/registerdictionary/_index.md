---
title: Hyphenation.RegisterDictionary
second_title: Aspose.Words for .NET API Referansı
description: Hyphenation yöntem. Bir akıştan belirtilen dil için bir tireleme sözlüğünü kaydeder ve yükler. Sözlüğün okunamaması veya biçiminin geçersiz olması durumunda hata oluşur.
type: docs
weight: 40
url: /tr/net/aspose.words/hyphenation/registerdictionary/
---
## RegisterDictionary(string, Stream) {#registerdictionary}

Bir akıştan belirtilen dil için bir tireleme sözlüğünü kaydeder ve yükler. Sözlüğün okunamaması veya biçiminin geçersiz olması durumunda hata oluşur.

```csharp
public static void RegisterDictionary(string language, Stream stream)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| language | String | Bir dil adı, örneğin "en-US". "Kültür adı" için .NET belgelerine ve ayrıntılar için RFC 4646'ya bakın. |
| stream | Stream | OpenOffice biçimindeki sözlük dosyası için bir akış. |

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

* class [Hyphenation](../)
* ad alanı [Aspose.Words](../../hyphenation/)
* toplantı [Aspose.Words](../../../)

---

## RegisterDictionary(string, string) {#registerdictionary_1}

Dosyadan belirtilen dil için bir tireleme sözlüğünü kaydeder ve yükler. Sözlüğün okunamaması veya biçiminin geçersiz olması durumunda hata oluşur.

Bu yöntem aynı zamanda Boş sözlüğü kaydetmek için de kullanılabilir.[`Callback`](../callback/) aynı dil için tekrar tekrar çağrılmayı önler.

```csharp
public static void RegisterDictionary(string language, string fileName)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| language | String | Bir dil adı, örneğin "en-US". "Kültür adı" için .NET belgelerine ve ayrıntılar için RFC 4646'ya bakın. |
| fileName | String | Open Office biçimindeki sözlük dosyasının yolu. |

### Örnekler

Bir tireleme sözlüğünün nasıl kaydedileceğini gösterir.

```csharp
// Bir tireleme sözlüğü, sözlüğün dili için tireleme kurallarını tanımlayan dizelerin bir listesini içerir.
// Bir belge, bir kelimenin bölünüp sonraki satırda devam edebileceği metin satırları içerdiğinde,
// tireleme, o kelimenin alt dizeleri için sözlüğün dize listesine bakacaktır.
// Sözlük bir alt dize içeriyorsa, tireleme sözcüğü iki satıra böler
// alt dizenin yanında ve ilk yarıya bir kısa çizgi ekleyin.
// Yerel dosya sisteminden bir sözlük dosyasını "de-CH" yerel ayarına kaydedin.
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Sözlüğümüzün yerel ayarıyla eşleşen metni içeren bir belge açın,
// ve onu sabit sayfa kaydetme formatında kaydedin. Bu belgedeki metin tirelenecektir.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Sözlüğün kaydını kaldırdıktan sonra belgeyi yeniden yükleyin,
// ve onu tireli metin içermeyecek başka bir PDF'ye kaydedin.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

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

* class [Hyphenation](../)
* ad alanı [Aspose.Words](../../hyphenation/)
* toplantı [Aspose.Words](../../../)


