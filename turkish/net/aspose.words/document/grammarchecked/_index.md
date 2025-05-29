---
title: Document.GrammarChecked
linktitle: GrammarChecked
articleTitle: GrammarChecked
second_title: .NET için Aspose.Words
description: GrammarChecked özelliğiyle belgenizin kalitesini garantileyin. Metninizin cilalı, profesyonel sonuçlar için dilbilgisi açısından doğrulanıp doğrulanmadığını keşfedin.
type: docs
weight: 190
url: /tr/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

Geri Döndürür`doğru` belgenin dil bilgisi açısından kontrol edilip edilmediği.

```csharp
public bool GrammarChecked { get; set; }
```

## Notlar

Belgedeki dilbilgisini yeniden denetlemek için bu özelliği şu şekilde ayarlayın:`YANLIŞ` .

## Örnekler

Yazım veya dilbilgisi doğrulamasının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Yazım hataları içeren dize.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

// Özellikleri false olarak ayarlarsak yazım/dilbilgisi denetimi başlar.
// Microsoft Word'deki tüm hataları İnceleme -> Yazım ve Dilbilgisi'nden görebiliriz.
// Microsoft Word'ün DOC ve RTF belge biçimleri için dilbilgisi/yazım denetimini otomatik olarak başlatmadığını unutmayın.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
