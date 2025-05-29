---
title: Document.LastSection
linktitle: LastSection
articleTitle: LastSection
second_title: .NET için Aspose.Words
description: Belgenizin son bölümüne kolayca erişmek, gezinme ve içerik yönetimi verimliliğini artırmak için LastSection özelliğini keşfedin.
type: docs
weight: 250
url: /tr/net/aspose.words/document/lastsection/
---
## Document.LastSection property

Belgedeki son bölümü alır.

```csharp
public Section LastSection { get; }
```

## Notlar

Geri Döndürür`hükümsüz`eğer bölüm yoksa.

## Örnekler

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

### Ayrıca bakınız

* class [Section](../../section/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
