---
title: PageSetup.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: .NET için Aspose.Words
description: Gelişmiş belge biçimlendirmesi ve netliği için son not numaralandırmasını ve konumlandırmasını kolayca özelleştirmek üzere PageSetup EndnoteOptions özelliğini keşfedin.
type: docs
weight: 120
url: /tr/net/aspose.words/pagesetup/endnoteoptions/
---
## PageSetup.EndnoteOptions property

Bu bölümdeki dipnotların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sağlar.

```csharp
public EndnoteOptions EndnoteOptions { get; }
```

## Örnekler

Bir bölümdeki dipnotları/sonnotları etkileyen seçeneklerin nasıl yapılandırılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote reference text.");

// İlk bölümdeki tüm dipnotları numaralandırmayı 1'den yeniden başlatacak şekilde yapılandırın
// her yeni sayfada ve her sayfadaki metnin hemen altında görüntülenir.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// Bölüm boyunca sürekli bir sayım sağlamak için ilk bölümdeki tüm dipnotları yapılandırın,
// 1'den başlayarak. Ayrıca, hepsinin belgenin sonunda toplanmış olarak görünmesini ayarlayın.
EndnoteOptions endnoteOptions = doc.Sections[0].PageSetup.EndnoteOptions;
endnoteOptions.Position = EndnotePosition.EndOfDocument;
endnoteOptions.RestartRule = FootnoteNumberingRule.Continuous;
endnoteOptions.StartNumber = 1;

doc.Save(ArtifactsDir + "PageSetup.FootnoteOptions.docx");
```

### Ayrıca bakınız

* class [EndnoteOptions](../../../aspose.words.notes/endnoteoptions/)
* class [PageSetup](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
