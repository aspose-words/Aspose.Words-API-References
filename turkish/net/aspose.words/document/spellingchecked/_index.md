---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: Aspose.Words for .NET
description: Document SpellingChecked mülk. İadelerdoğru belgenin yazım denetimi yapılmışsa C#'da.
type: docs
weight: 410
url: /tr/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

İadeler`doğru` belgenin yazım denetimi yapılmışsa.

```csharp
public bool SpellingChecked { get; set; }
```

## Notlar

Belgedeki yazımı yeniden denetlemek için bu özelliği şu şekilde ayarlayın:`YANLIŞ` .

## Örnekler

Yazım veya dil bilgisi doğrulamanın nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Yazım hatası içeren dize.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

 // Özellikleri false olarak ayarlarsak Yazım/Dilbilgisi denetimi başlar.
// Microsoft Word'deki tüm hataları İnceleme --> aracılığıyla görebiliriz. Yazım ve amp; Dilbilgisi.
// Microsoft Word'ün DOC ve RTF belge formatı için dilbilgisi/yazım denetimini otomatik olarak başlatmadığını unutmayın.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
