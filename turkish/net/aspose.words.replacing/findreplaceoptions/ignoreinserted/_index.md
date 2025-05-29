---
title: FindReplaceOptions.IgnoreInserted
linktitle: IgnoreInserted
articleTitle: IgnoreInserted
second_title: .NET için Aspose.Words
description: FindReplaceOptions IgnoreInserted özelliğini keşfedin, bu basit boolean ayarıyla ekleme revizyonlarında metin işlemeyi kontrol edin. Varsayılan değer false'tur.
type: docs
weight: 100
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignoreinserted/
---
## FindReplaceOptions.IgnoreInserted property

Ekleme revizyonları içindeki metni yoksaymayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool IgnoreInserted { get; set; }
```

## Örnekler

Bul ve değiştir işlemi sırasında ekleme revizyonlarının içine metin ekleme veya yok sayma işleminin nasıl yapılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Hello world!");

// Revizyonları izlemeye başla ve bir paragraf ekle. Bu paragraf bir ekleme revizyonu olacak.
doc.StartTrackRevisions("John Doe", DateTime.Now);
builder.Writeln("Hello again!");
doc.StopTrackRevisions();

Assert.True(doc.FirstSection.Body.Paragraphs[1].IsInsertRevision);

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Bul ve değiştir özelliğini elde etmek için "IgnoreInserted" bayrağını "true" olarak ayarlayın
// ekleme revizyonları olan paragrafları yok sayma işlemi.
// Bul ve değiştir özelliğini elde etmek için "IgnoreInserted" bayrağını "false" olarak ayarlayın
// insert revizyonlarının içinde metin arama işlemi.
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
