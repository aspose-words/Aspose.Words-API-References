---
title: ParagraphFormat.SuppressAutoHyphens
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Geçerli paragrafın belge ayarlarında uygulanan herhangi bir tirelemeden muaf tutulup tutulmayacağını belirtir.
type: docs
weight: 360
url: /tr/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Geçerli paragrafın, belge ayarlarında uygulanan herhangi bir tirelemeden muaf tutulup tutulmayacağını belirtir.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

### Örnekler

Bir paragraf için tirelemenin nasıl bastırılacağını gösterir.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Sözlüğümüzün yerel ayarıyla eşleşen metin içeren bir belge açın.
// Bu belgeyi sabit bir sayfa kaydetme biçiminde kaydettiğimizde, metninde tireleme olacaktır.
Document doc = new Document(MyDir + "German text.docx");

// Tirelemeyi devre dışı bırakmak için "SuppressAutoHyphens" özelliğini "true" olarak ayarlayabiliriz
// belgenin geri kalanı için etkin halde tutarken belirli bir paragraf için.
// Bu özelliğin varsayılan değeri "false"dır,
// bu, varsa her paragrafın varsayılan olarak tirelemeyi kullandığı anlamına gelir.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


