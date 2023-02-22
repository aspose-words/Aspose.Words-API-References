---
title: Document.SpellingChecked
second_title: Aspose.Words for .NET API Referansı
description: Document mülk. İade doğru belgenin yazım denetimi yapıldıysa.
type: docs
weight: 390
url: /tr/net/aspose.words/document/spellingchecked/
---
## Document.SpellingChecked property

İade **doğru** belgenin yazım denetimi yapıldıysa.

```csharp
public bool SpellingChecked { get; set; }
```

### Notlar

Belgedeki yazımı yeniden kontrol etmek için bu özelliği **yanlış** .

### Örnekler

Yazım veya dil bilgisi doğrulamasının nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();

// Yazım hataları olan dize.
doc.FirstSection.Body.FirstParagraph.Runs.Add(new Run(doc, "The speeling in this documentz is all broked."));

 // Özellikleri false olarak ayarlarsak Yazım/Dilbilgisi denetimi başlar.
// Microsoft Word'deki tüm hataları İnceleme -> Yazım & Dilbilgisi.
// Microsoft Word'ün DOC ve RTF belge formatı için dilbilgisi/yazım denetimini otomatik olarak başlatmadığını unutmayın.
doc.SpellingChecked = checkSpellingGrammar;
doc.GrammarChecked = checkSpellingGrammar;

doc.Save(ArtifactsDir + "Document.SpellingOrGrammar.docx");
```

### Ayrıca bakınız

* class [Document](../)
* ad alanı [Aspose.Words](../../document/)
* toplantı [Aspose.Words](../../../)


