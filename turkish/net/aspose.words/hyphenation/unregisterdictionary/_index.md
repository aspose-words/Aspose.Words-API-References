---
title: Hyphenation.UnregisterDictionary
linktitle: UnregisterDictionary
articleTitle: UnregisterDictionary
second_title: .NET için Aspose.Words
description: UnregisterDictionary yöntemi ile herhangi bir dil için tireleme sözlüklerini zahmetsizce kaldırın, metnin anlaşılırlığını ve okunabilirliğini artırın.
type: docs
weight: 50
url: /tr/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

Belirtilen dil için bir tireleme sözlüğünün kaydını siler.

Bu, Null sözlüğünün kaydedilmesinden farklıdır. Bir sözlüğün kaydının silinmesi, belirtilen dil için geri aramayı etkinleştirir.

```csharp
public static void UnregisterDictionary(string language)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| language | String | Bir dil adı, örneğin "en-US". "Kültür adı" için .NET belgelerine ve ayrıntılar için RFC 4646'ya bakın. |

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
