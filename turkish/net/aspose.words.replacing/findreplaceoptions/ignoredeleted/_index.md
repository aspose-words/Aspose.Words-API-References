---
title: FindReplaceOptions.IgnoreDeleted
linktitle: IgnoreDeleted
articleTitle: IgnoreDeleted
second_title: .NET için Aspose.Words
description: FindReplaceOptions IgnoreDeleted özelliğini keşfedin, silinen revizyonlardaki metin görünürlüğünü kolay bir Boole geçişiyle kontrol edin. Düzenleme deneyiminizi geliştirin!
type: docs
weight: 60
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignoredeleted/
---
## FindReplaceOptions.IgnoreDeleted property

Silinen revizyonların içindeki metni yoksaymayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool IgnoreDeleted { get; set; }
```

## Örnekler

Bir bul ve değiştir işlemi sırasında silme revizyonlarının içindeki metnin nasıl ekleneceğini veya yoksayılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");
builder.Writeln("Hello again!");

// Revizyonları izlemeye başla ve ikinci paragrafı kaldır, bu bir silme revizyonu yaratacaktır.
// Bu paragraf, silme revizyonunu kabul edene kadar belgede kalacaktır.
doc.StartTrackRevisions("John Doe", DateTime.Now);
doc.FirstSection.Body.Paragraphs[1].Remove();
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsDeleteRevision);

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Bul ve değiştir özelliğini elde etmek için "IgnoreDeleted" bayrağını "true" olarak ayarlayın
// silme revizyonları olan paragrafları yok sayma işlemi.
// Bul ve değiştir özelliğini elde etmek için "IgnoreDeleted" bayrağını "false" olarak ayarlayın
// silme revizyonlarının içinde de metin arama işlemi.
options.IgnoreDeleted = ignoreTextInsideDeleteRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideDeleteRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
