---
title: Document.FirstSection
linktitle: FirstSection
articleTitle: FirstSection
second_title: .NET için Aspose.Words
description: Belgenizin ilk bölümünü zahmetsizce alın. Sorunsuz bir organizasyon için Document FirstSection özelliğimizle iş akışınızı geliştirin.
type: docs
weight: 140
url: /tr/net/aspose.words/document/firstsection/
---
## Document.FirstSection property

Belgedeki ilk bölümü alır.

```csharp
public Section FirstSection { get; }
```

## Notlar

Geri Döndürür`hükümsüz`eğer bölüm yoksa.

## Örnekler

Bir belgenin altbilgisindeki metnin nasıl değiştirileceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Footer.docx");

HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
HeaderFooter footer = headersFooters[HeaderFooterType.FooterPrimary];

FindReplaceOptions options = new FindReplaceOptions
{
    MatchCase = false,
    FindWholeWordsOnly = false
};

int currentYear = DateTime.Now.Year;
footer.Range.Replace("(C) 2006 Aspose Pty Ltd.", $"Copyright (C) {currentYear} by Aspose Pty Ltd.", options);

doc.Save(ArtifactsDir + "HeaderFooter.ReplaceText.docx");
```

Belge oluşturucuyla yeni bir bölümün nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();

// Boş bir belge varsayılan olarak bir bölüm içerir,
// düzenleyebileceğimiz alt düğümleri içerir.
Assert.AreEqual(1, doc.Sections.Count);

// İlk bölüme metin eklemek için bir belge oluşturucu kullanın.
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Bölüm sonu ekleyerek ikinci bir bölüm oluşturun.
builder.InsertBreak(BreakType.SectionBreakNewPage);

Assert.AreEqual(2, doc.Sections.Count);

// Her bölümün kendine özgü sayfa düzeni ayarları vardır.
// İkinci bölümdeki metni iki sütuna bölebiliriz.
// Bu, ilk bölümdeki metni etkilemeyecektir.
doc.LastSection.PageSetup.TextColumns.SetCount(2);
builder.Writeln("Column 1.");
builder.InsertBreak(BreakType.ColumnBreak);
builder.Writeln("Column 2.");

Assert.AreEqual(1, doc.FirstSection.PageSetup.TextColumns.Count);
Assert.AreEqual(2, doc.LastSection.PageSetup.TextColumns.Count);

doc.Save(ArtifactsDir + "Section.Create.docx");
```

Bir bileşik düğümün alt düğümleri arasında nasıl yineleme yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Section 1");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Primary header");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Write("Primary footer");

Section section = doc.FirstSection;

// Bir Bölüm, bileşik bir düğümdür ve alt düğümler içerebilir,
// ancak yalnızca bu alt düğümler "Body" veya "HeaderFooter" düğüm türündeyse.
foreach (Node node in section)
{
    switch (node.NodeType)
    {
        case NodeType.Body:
        {
            Body body = (Body)node;

            Console.WriteLine("Body:");
            Console.WriteLine($"\t\"{body.GetText().Trim()}\"");
            break;
        }
        case NodeType.HeaderFooter:
        {
            HeaderFooter headerFooter = (HeaderFooter)node;

            Console.WriteLine($"HeaderFooter type: {headerFooter.HeaderFooterType}:");
            Console.WriteLine($"\t\"{headerFooter.GetText().Trim()}\"");
            break;
        }
        default:
        {
            throw new Exception("Unexpected node type in a section.");
        }
    }
}
```

### Ayrıca bakınız

* class [Section](../../section/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
