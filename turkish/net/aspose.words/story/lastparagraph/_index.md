---
title: Story.LastParagraph
second_title: Aspose.Words for .NET API Referansı
description: Story mülk. Öyküdeki son paragrafı alır.
type: docs
weight: 20
url: /tr/net/aspose.words/story/lastparagraph/
---
## Story.LastParagraph property

Öyküdeki son paragrafı alır.

```csharp
public Paragraph LastParagraph { get; }
```

### Örnekler

DocumentBuilder'ın imleç konumunun belirli bir düğüme nasıl taşınacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Run 1. ");

// Belge oluşturucu, belgenin parçası olarak işlev gören bir imleç içerir
// belge oluşturma yöntemlerini kullandığımızda oluşturucunun yeni düğümler eklediği yer.
// Bu imleç, Microsoft Word'ün yanıp sönen imleciyle aynı şekilde çalışır,
// ve ayrıca her zaman oluşturucunun yeni eklediği herhangi bir düğümden hemen sonra biter.
// Belgenin farklı bir bölümüne içerik eklemek için,
// "MoveTo" yöntemi ile imleci farklı bir düğüme taşıyabiliriz.
// İmleç şimdi onu taşıdığımız düğümün önündedir.
// İkinci bir çalıştırma eklemek, onu ilk çalıştırmanın önüne ekleyecektir.
builder.Writeln("Run 2. ");

Assert.AreEqual("Run 2. \rRun 1.", doc.GetText().Trim());

// Daha önce olduğu gibi sonuna metin eklemeye devam etmek için imleci belgenin sonuna taşıyın.
builder.MoveTo(doc.LastSection.Body.LastParagraph);
builder.Writeln("Run 3. ");

Assert.AreEqual("Run 2. \rRun 1. \rRun 3.", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Paragraph](../../paragraph/)
* class [Story](../)
* ad alanı [Aspose.Words](../../story/)
* toplantı [Aspose.Words](../../../)


