---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: .NET için Aspose.Words
description: Hyphenation IsDictionaryRegistered metodunu keşfedin, uygulamalarınızda doğru tirelemeyi garantilemek için bir sözlüğün diliniz için kayıtlı olup olmadığını kontrol eder.
type: docs
weight: 30
url: /tr/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

Geri Döndürür`YANLIŞ` Belirtilen dil için kayıtlı bir sözlük yoksa veya kayıtlı sözlük Null ise,`doğru` aksi takdirde.

```csharp
public static bool IsDictionaryRegistered(string language)
```

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

### Ayrıca bakınız

* class [Hyphenation](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
