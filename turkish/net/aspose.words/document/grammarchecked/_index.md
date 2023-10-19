---
title: Document.GrammarChecked
linktitle: GrammarChecked
articleTitle: GrammarChecked
second_title: Aspose.Words for .NET
description: Document GrammarChecked mülk. İadelerdoğru belge dilbilgisi açısından kontrol edilmişse C#'da.
type: docs
weight: 180
url: /tr/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

İadeler`doğru` belge dilbilgisi açısından kontrol edilmişse.

```csharp
public bool GrammarChecked { get; set; }
```

## Notlar

Belgedeki dilbilgisini yeniden kontrol etmek için bu özelliği şu şekilde ayarlayın:`YANLIŞ` .

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
