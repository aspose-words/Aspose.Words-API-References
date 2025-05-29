---
title: FramesetCollection.Item
linktitle: Item
articleTitle: Item
second_title: .NET için Aspose.Words
description: FramesetCollection ile belirli çerçevelere erişin. Verimli web gezintisi ve gelişmiş kullanıcı deneyimi için çerçeve sayfalarını dizine göre kolayca alın.
type: docs
weight: 30
url: /tr/net/aspose.words.framesets/framesetcollection/item/
---
## FramesetCollection indexer

Belirtilen dizinde bir çerçeve veya çerçeveler sayfası alır.

```csharp
public Frameset this[int index] { get; }
```

## Örnekler

Sayfadaki çerçevelere nasıl erişileceğini gösterir.

```csharp
// Belge, diğer belgelere bağlantılar içeren birkaç çerçeve içeriyor.
Document doc = new Document(MyDir + "Frameset.docx");

Assert.AreEqual(3, doc.Frameset.ChildFramesets.Count);
// Varsayılan URL'yi (bir web sayfası URL'si veya yerel belge) veya çerçevenin harici bir kaynak olup olmadığını kontrol edebiliriz.
Assert.AreEqual("https://dosya-ornekleri-com.github.io/uploads/2017/02/dosya-ornegi_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Çerçevelerimizden birinin özelliklerini değiştirelim.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Mutlak%20konum%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Ayrıca bakınız

* class [Frameset](../../frameset/)
* class [FramesetCollection](../)
* ad alanı [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* toplantı [Aspose.Words](../../../)
