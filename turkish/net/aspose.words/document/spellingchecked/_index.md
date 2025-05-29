---
title: Document.SpellingChecked
linktitle: SpellingChecked
articleTitle: SpellingChecked
second_title: .NET için Aspose.Words
description: SpellingChecked özelliğiyle belgenizin hatasız olduğundan emin olun. İçeriğinizin profesyonellik açısından kapsamlı bir şekilde yazım denetiminden geçirilip geçirilmediğini keşfedin.
type: docs
weight: 430
url: /tr/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

Geri Döndürür`doğru` belgenin yazım denetimi yapılmışsa.

```csharp
public bool SpellingChecked { get; set; }
```

## Notlar

Belgedeki yazımı yeniden denetlemek için bu özelliği şu şekilde ayarlayın:`YANLIŞ` .

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
