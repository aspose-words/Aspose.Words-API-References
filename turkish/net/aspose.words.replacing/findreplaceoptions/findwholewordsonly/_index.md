---
title: FindReplaceOptions.FindWholeWordsOnly
linktitle: FindWholeWordsOnly
articleTitle: FindWholeWordsOnly
second_title: .NET için Aspose.Words
description: FindWholeWordsOnly özelliğinin, oldValue'nun yalnızca tek başına bir sözcük olarak eşleşmesini sağlayarak aramanızı nasıl doğru sonuçlarla geliştirdiğini keşfedin.
type: docs
weight: 50
url: /tr/net/aspose.words.replacing/findreplaceoptions/findwholewordsonly/
---
## FindReplaceOptions.FindWholeWordsOnly property

True, eskiDeğer'in bağımsız bir sözcük olması gerektiğini belirtir.

```csharp
public bool FindWholeWordsOnly { get; set; }
```

## Örnekler

Bağımsız kelime bazlı bul ve değiştir işlemlerinin nasıl açılıp kapatılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Writeln("Jackson will meet you in Jacksonville.");

// Bul ve değiştir işlemini değiştirmek için "FindReplaceOptions" nesnesini kullanabiliriz.
FindReplaceOptions options = new FindReplaceOptions();

// Bulunan metin başka bir kelimenin parçası değilse, onu değiştirmek için "FindWholeWordsOnly" bayrağını "true" olarak ayarlayın.
// Çevresindekilere bakılmaksızın tüm metni değiştirmek için "FindWholeWordsOnly" bayrağını "false" olarak ayarlayın.
options.FindWholeWordsOnly = findWholeWordsOnly;

doc.Range.Replace("Jackson", "Louis", options);

Assert.AreEqual(
    findWholeWordsOnly ? "Louis will meet you in Jacksonville." : "Louis will meet you in Louisville.",
    doc.GetText().Trim());
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
