---
title: FindReplaceOptions.IgnoreFootnotes
linktitle: IgnoreFootnotes
articleTitle: IgnoreFootnotes
second_title: Aspose.Words for .NET
description: FindReplaceOptions IgnoreFootnotes mülk. Dipnotların yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değerYANLIŞ  C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Dipnotların yoksayılacağını belirten bir boole değeri alır veya ayarlar. Varsayılan değer:`YANLIŞ` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

## Örnekler

Bul ve değiştir işlemi sırasında dipnotların nasıl yok sayılacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Bul ve değiştir işlevini elde etmek için "IgnoreFootnotes" bayrağını "true" olarak ayarlayın
// dipnotların içindeki metni yok sayma işlemi.
// Bul ve değiştir işlevini elde etmek için "IgnoreFootnotes" bayrağını "false" olarak ayarlayın
// dipnotların içindeki metni de arama işlemi.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
