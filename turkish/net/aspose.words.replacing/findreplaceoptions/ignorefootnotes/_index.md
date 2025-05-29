---
title: FindReplaceOptions.IgnoreFootnotes
linktitle: IgnoreFootnotes
articleTitle: IgnoreFootnotes
second_title: .NET için Aspose.Words
description: Belgelerinizdeki dipnotları kolayca yönetmek için FindReplaceOptions IgnoreFootnotes özelliğini keşfedin. Bu basit geçişle düzenleme verimliliğini artırın!
type: docs
weight: 90
url: /tr/net/aspose.words.replacing/findreplaceoptions/ignorefootnotes/
---
## FindReplaceOptions.IgnoreFootnotes property

Dipnotları yoksaymayı belirten bir Boole değeri alır veya ayarlar. Varsayılan değer`YANLIŞ` .

```csharp
public bool IgnoreFootnotes { get; set; }
```

## Örnekler

Bul ve değiştir işlemi sırasında dipnotların nasıl göz ardı edileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Footnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

builder.InsertParagraph();

builder.Write("Lorem ipsum dolor sit amet, consectetur adipiscing elit.");
builder.InsertFootnote(FootnoteType.Endnote, "Lorem ipsum dolor sit amet, consectetur adipiscing elit.");

// Bul ve değiştir özelliğini elde etmek için "IgnoreFootnotes" bayrağını "true" olarak ayarlayın
// dipnotların içindeki metni yok sayma işlemi.
// Bul ve değiştir özelliğini elde etmek için "IgnoreFootnotes" bayrağını "false" olarak ayarlayın
// Dipnotların içindeki metni de arama işlemi.
FindReplaceOptions options = new FindReplaceOptions { IgnoreFootnotes = isIgnoreFootnotes };
doc.Range.Replace("Lorem ipsum", "Replaced Lorem ipsum", options);
```

### Ayrıca bakınız

* class [FindReplaceOptions](../)
* ad alanı [Aspose.Words.Replacing](../../../aspose.words.replacing/)
* toplantı [Aspose.Words](../../../)
