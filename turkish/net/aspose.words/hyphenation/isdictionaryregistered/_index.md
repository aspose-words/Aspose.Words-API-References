---
title: Hyphenation.IsDictionaryRegistered
second_title: Aspose.Words for .NET API Referansı
description: Hyphenation yöntem. Belirtilen dil için kayıtlı sözlük yoksa veya kayıtlıysa Null sözlük ise False aksi takdirde True döndürür.
type: docs
weight: 30
url: /tr/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Belirtilen dil için kayıtlı sözlük yoksa veya kayıtlıysa Null sözlük ise False, aksi takdirde True döndürür.

```csharp
public static bool IsDictionaryRegistered(string language)
```

### Örnekler

Tireleme sözlüğünün nasıl kaydedileceğini gösterir.

```csharp
// Tireleme sözlüğü, sözlüğün dili için tireleme kurallarını tanımlayan dizelerin bir listesini içerir.
// Bir belge, bir kelimenin bölünebileceği ve bir sonraki satırda devam edebileceği metin satırları içerdiğinde,
// tireleme, o kelimenin alt dizeleri için sözlüğün dize listesine bakacaktır.
// Sözlük bir alt dize içeriyorsa, tireleme sözcüğü iki satıra böler
// alt dizeye göre ve ilk yarıya kısa çizgi ekleyin.
// Yerel dosya sisteminden bir sözlük dosyasını "de-CH" yerel ayarına kaydedin.
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Sözlüğümüzün yerel ayarıyla eşleşen metin içeren bir belge açın,
// ve sabit sayfa kaydetme biçiminde kaydedin. Bu belgedeki metin tirelenir.
Document doc = new Document(MyDir + "German text.docx");

Assert.True(doc.FirstSection.Body.FirstParagraph.Runs.OfType<Run>().All(
    r => r.Font.LocaleId == new CultureInfo("de-CH").LCID));

doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Registered.pdf");

// Sözlüğün kaydını sildikten sonra belgeyi yeniden yükleyin,
// ve onu tireli metne sahip olmayacak başka bir PDF'ye kaydedin.
Hyphenation.UnregisterDictionary("de-CH");

Assert.False(Hyphenation.IsDictionaryRegistered("de-CH"));

doc = new Document(MyDir + "German text.docx");
doc.Save(ArtifactsDir + "Hyphenation.Dictionary.Unregistered.pdf");
```

### Ayrıca bakınız

* class [Hyphenation](../)
* ad alanı [Aspose.Words](../../hyphenation/)
* toplantı [Aspose.Words](../../../)


