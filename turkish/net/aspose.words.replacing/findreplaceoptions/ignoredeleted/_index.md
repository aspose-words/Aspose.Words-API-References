---
title: FindReplaceOptions.IgnoreDeleted
second_title: Aspose.Words for .NET API Referansı
description: FindReplaceOptions mülk. Silme düzeltmeleri içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değerYANLIŞ .
type: docs
weight: 60
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Silme düzeltmeleri içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` .

```csharp
public bool IgnoreDeleted { get; set; }
```

### Örnekler

Bul ve değiştir işlemi sırasında düzeltmelerin içine metnin nasıl dahil edileceğini veya yok sayılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Revizyonları izlemeye başlayın ve revizyonun silinmesini sağlayacak ikinci paragrafı kaldırın.
// Bu paragraf biz silme revizyonunu kabul edene kadar belgede kalacaktır.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Bul ve değiştir işlevini elde etmek için "IgnoreDeleted" bayrağını "true" olarak ayarlayın
// revizyonları silen paragrafları yok sayma işlemi.
// Bul ve değiştir işlevini almak için "IgnoreDeleted" bayrağını "false" olarak ayarlayın
// düzeltmelerin silinmesi içindeki metni de arama işlemi.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../findreplaceoptions/)
* toplantı [Aspose.Words](../../../)


