---
title: Hyphenation.IsDictionaryRegistered
linktitle: IsDictionaryRegistered
articleTitle: IsDictionaryRegistered
second_title: Aspose.Words for .NET
description: Hyphenation IsDictionaryRegistered yöntem. İadelerYANLIŞ belirtilen dil için kayıtlı sözlük yoksa veya kayıtlıysa Boş sözlük isedoğru aksi halde C#'da.
type: docs
weight: 30
url: /tr/net/aspose.words/hyphenation/isdictionaryregistered/
---
## Hyphenation.IsDictionaryRegistered method

İadeler`YANLIŞ` belirtilen dil için kayıtlı sözlük yoksa veya kayıtlıysa Boş sözlük ise,`doğru` aksi halde.

```csharp
public static bool IsDictionaryRegistered(string language)
```

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
