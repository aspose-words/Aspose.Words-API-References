---
title: Story.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: .NET için Aspose.Words
description: Hikayenizin son paragrafına Story LastParagraph özelliğiyle zahmetsizce ulaşın, anlatı yönetimi ve düzenleme deneyiminizi geliştirin.
type: docs
weight: 20
url: /tr/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Hikayedeki son paragrafı alır.

```csharp
public Paragraph LastParagraph { get; }
```

## Örnekler

Bir DocumentBuilder'ın imleç konumunun belirtilen bir düğüme nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Belge oluşturucunun, belgenin bir parçası olarak işlev gören bir imleci vardır
// Oluşturucunun belge oluşturma yöntemlerini kullandığımızda yeni düğümler eklediği yer.
// Bu imleç, Microsoft Word'ün yanıp sönen imleciyle aynı şekilde çalışır,
// ve ayrıca her zaman oluşturucunun eklediği herhangi bir düğümün hemen ardından sonlanır.
// Belgenin farklı bir bölümüne içerik eklemek için,
// "MoveTo" metodu ile imleci farklı bir düğüme taşıyabiliriz.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// İmleç artık onu taşıdığımız düğümün önünde.
// İkinci bir çalışma eklemek, onu ilk çalışmanın önüne ekleyecektir.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Metni daha önce olduğu gibi belgenin sonuna eklemeye devam etmek için imleci belgenin sonuna getirin.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Paragraph](../../paragraph/)
* class [Story](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
