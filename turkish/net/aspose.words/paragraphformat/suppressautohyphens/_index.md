---
title: ParagraphFormat.SuppressAutoHyphens
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Geçerli paragrafın belge ayarlarında uygulanan herhangi bir tirelemeden muaf tutulması gerekip gerekmediğini belirtir.
type: docs
weight: 370
url: /tr/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Geçerli paragrafın, belge ayarlarında uygulanan herhangi bir tirelemeden muaf tutulması gerekip gerekmediğini belirtir.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

### Örnekler

Bir paragrafta tirelemenin nasıl bastırılacağını gösterir.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Sözlüğümüzün yerel ayarıyla eşleşen metni içeren bir belge açın.
// Bu belgeyi sabit sayfa kaydetme formatında kaydettiğimizde metninde tireleme olacaktır.
Document doc = new Document(MyDir + "German text.docx");

// Tirelemeyi devre dışı bırakmak için "SuppressAutoHyphens" özelliğini "true" olarak ayarlayabiliriz
// belirli bir paragraf için bunu belgenin geri kalanı için etkin tutarken.
// Bu özelliğin varsayılan değeri "yanlış"tır,
// bu, varsa her paragrafın varsayılan olarak tirelemeyi kullandığı anlamına gelir.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


