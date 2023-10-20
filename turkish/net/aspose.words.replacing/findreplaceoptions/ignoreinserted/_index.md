---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: Aspose.Words for .NET
description: FindReplaceOptions IgnoreInserted mülk. Ekleme düzeltmeleri içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değerYANLIŞ  C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Ekleme düzeltmeleri içindeki metnin yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` .

```csharp
public bool IgnoreInserted { get; set; }
```

## Örnekler

Bul ve değiştir işlemi sırasında ekleme düzeltmelerinin içine metnin nasıl dahil edileceğini veya yok sayılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Revizyonları izlemeye başlayın ve bir paragraf ekleyin. Bu paragraf bir ekleme revizyonu olacaktır.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Bul ve değiştir işlemini değiştirmek için bir "FindReplaceOptions" nesnesi kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Bul ve değiştir işlevini elde etmek için "IgnoreInserted" bayrağını "true" olarak ayarlayın
// düzeltme ekleyen paragrafları yok sayma işlemi.
// Bul ve değiştir işlevini elde etmek için "IgnoreInserted" bayrağını "false" olarak ayarlayın
// düzeltme eklemelerin içindeki metni de arama işlemi.
options.IgnoreInserted = ignoreTextInsideInsertRevisions;

doc.Range.Replace("Hello", "Greetings", options);

Assert.AreEqual(
    ignoreTextInsideInsertRevisions
        ? "Greetings world!\rHello again!"
        : "Greetings world!\rGreetings again!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
