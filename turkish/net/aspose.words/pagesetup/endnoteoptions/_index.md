---
title: PageSetup.EndnoteOptions
linktitle: EndnoteOptions
articleTitle: EndnoteOptions
second_title: Aspose.Words for .NET
description: PageSetup EndnoteOptions mülk. Bu bölümdeki son notların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sunar C#'da.
type: docs
weight: 120
url: /tr/net/aspose.words/pagesetup/endnoteoptions/
---
## PageSetup.EndnoteOptions property

Bu bölümdeki son notların numaralandırılmasını ve konumlandırılmasını kontrol eden seçenekler sunar.

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

// Numaralandırmayı 1'den yeniden başlatmak için ilk bölümdeki tüm dipnotları yapılandırın
// her yeni sayfada ve kendilerini her sayfada doğrudan metnin altında görüntüler.
FootnoteOptions footnoteOptions = doc.Sections[0].PageSetup.FootnoteOptions;
footnoteOptions.Position = FootnotePosition.BeneathText;
footnoteOptions.RestartRule = FootnoteNumberingRule.RestartPage;
footnoteOptions.StartNumber = 1;

builder.Write(" Hello again.");
builder.InsertFootnote(FootnoteType.Footnote, "Endnote reference text.");

// Bölüm boyunca sürekli bir sayım sağlamak için ilk bölümdeki tüm son notları yapılandırın,
// 1'den başlayarak. Ayrıca hepsini belgenin sonunda toplu olarak görünecek şekilde ayarlayın.
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
