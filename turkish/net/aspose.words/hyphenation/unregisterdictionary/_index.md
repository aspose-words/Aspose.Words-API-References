---
title: Hyphenation.UnregisterDictionary
linktitle: UnregisterDictionary
articleTitle: UnregisterDictionary
second_title: Aspose.Words for .NET
description: Hyphenation UnregisterDictionary yöntem. Belirtilen dil için tireleme sözlüğünün kaydını siler C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words/hyphenation/unregisterdictionary/
---
## Hyphenation.UnregisterDictionary method

Belirtilen dil için tireleme sözlüğünün kaydını siler.

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

### Ayrıca bakınız

* class [Hyphenation](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
