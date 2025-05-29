---
title: ParagraphFormat.SuppressAutoHyphens
linktitle: SuppressAutoHyphens
articleTitle: SuppressAutoHyphens
second_title: .NET için Aspose.Words
description: ParagraphFormat SuppressAutoHyphens özelliğiyle belgenizdeki tirelemeyi kontrol edin, net ve profesyonel paragraf biçimlendirmesini garantileyin.
type: docs
weight: 380
url: /tr/net/aspose.words/paragraphformat/suppressautohyphens/
---
## ParagraphFormat.SuppressAutoHyphens property

Geçerli paragrafın, belge ayarlarında uygulanan herhangi bir tirelemeden muaf tutulup tutulmayacağını belirtir.

```csharp
public bool SuppressAutoHyphens { get; set; }
```

## Örnekler

Bir paragrafta tirelemenin nasıl bastırılacağını gösterir.

```csharp
Hyphenation.RegisterDictionary("de-CH", MyDir + "hyph_de_CH.dic");

Assert.True(Hyphenation.IsDictionaryRegistered("de-CH"));

// Sözlüğümüzle eşleşen bir yerel ayara sahip metin içeren bir belge açın.
// Bu belgeyi sabit sayfa kaydetme biçimine kaydettiğimizde, metninde tireleme olacaktır.
Document doc = new Document(MyDir + "German text.docx");

// Tirelemeyi devre dışı bırakmak için "SuppressAutoHyphens" özelliğini "true" olarak ayarlayabiliriz
// belirli bir paragraf için etkin kalırken, belgenin geri kalanında etkin kalır.
// Bu özelliğin varsayılan değeri "false"dur,
// bu, her paragrafın varsayılan olarak varsa tirelemeyi kullandığı anlamına gelir.
doc.FirstSection.Body.FirstParagraph.ParagraphFormat.SuppressAutoHyphens = suppressAutoHyphens;

doc.Save(ArtifactsDir + "ParagraphFormat.SuppressHyphens.pdf");
```

### Ayrıca bakınız

* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
