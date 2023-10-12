---
title: Story.LastParagraph
second_title: Aspose.Words for .NET API Referansı
description: Story mülk. Hikayedeki son paragrafı alır.
type: docs
weight: 20
url: /tr/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Hikayedeki son paragrafı alır.

```csharp
public Paragraph LastParagraph { get; }
```

### Örnekler

DocumentBuilder'ın imleç konumunun belirli bir düğüme nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Belge oluşturucunun belgenin bir parçası olarak görev yapan bir imleci vardır
// belge oluşturma yöntemlerini kullandığımızda oluşturucunun yeni düğümler eklediği yer.
// Bu imleç Microsoft Word'ün yanıp sönen imleciyle aynı şekilde çalışır,
// ve ayrıca her zaman oluşturucunun az önce eklediği herhangi bir düğümden hemen sonra biter.
// Belgenin farklı bir bölümüne içerik eklemek için,
// "MoveTo" metodu ile imleci farklı bir düğüme taşıyabiliriz.
builder.MoveTo(doc.FirstSection.Body.FirstParagraph.Runs[0]);
// İmleç artık onu taşıdığımız düğümün önünde.
// İkinci bir çalıştırmanın eklenmesi onu ilk çalıştırmanın önüne ekleyecektir.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Metni daha önce olduğu gibi sonuna eklemeye devam etmek için imleci belgenin sonuna taşıyın.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Paragraph](../../paragraph/)
* class [Story](../)
* ad alanı [Aspose.Words](../../story/)
* toplantı [Aspose.Words](../../../)


