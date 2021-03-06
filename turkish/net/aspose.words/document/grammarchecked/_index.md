---
title: GrammarChecked
second_title: Aspose.Words for .NET API Referansı
description: İade doğru belge gramer açısından kontrol edilmişse.
type: docs
weight: 180
url: /tr/net/aspose.words/document/grammarchecked/
---
## Document.GrammarChecked property

İade **doğru** belge gramer açısından kontrol edilmişse.

```csharp
public bool GrammarChecked { get; set; }
```

### Notlar

Belgedeki dil bilgisini yeniden kontrol etmek için bu özelliği **yanlış** .

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

* class [Document](../../document)
* ad alanı [Aspose.Words](../../document)
* toplantı [Aspose.Words](../../../)

<!-- DO NOT EDIT: generated by xmldocmd for Aspose.Words.dll -->
