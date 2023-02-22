---
title: Frameset.ChildFramesets
second_title: Aspose.Words for .NET API Referansı
description: Frameset mülk. Alt çerçeveler ve çerçeve sayfaları koleksiyonunu alır.
type: docs
weight: 20
url: /tr/net/aspose.words.framesets/frameset/childframesets/
---
## Frameset.ChildFramesets property

Alt çerçeveler ve çerçeve sayfaları koleksiyonunu alır.

```csharp
public FramesetCollection ChildFramesets { get; }
```

### Örnekler

Sayfadaki çerçevelere nasıl erişileceğini gösterir.

```csharp
// Belge, diğer belgelere bağlantı içeren birkaç çerçeve içeriyor.
Document doc = new Document(MyDir + "Frameset.docx");

// Varsayılan URL'yi (bir web sayfası URL'si veya yerel belge) veya çerçevenin harici bir kaynak olup olmadığını kontrol edebiliriz.
Assert.AreEqual("https://file-examples-com.github.io/uploads/2017/02/file-sample_100kB.docx",
    doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl);
Assert.True(doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile);

Assert.AreEqual("Document.docx", doc.Frameset.ChildFramesets[1].FrameDefaultUrl);
Assert.False(doc.Frameset.ChildFramesets[1].IsFrameLinkToFile);

// Çerçevelerimizden birinin özelliklerini değiştirin.
doc.Frameset.ChildFramesets[0].ChildFramesets[0].FrameDefaultUrl =
    "https://github.com/aspose-words/Aspose.Words-for-.NET/blob/master/Examples/Data/Absolute%20position%20tab.docx";
doc.Frameset.ChildFramesets[0].ChildFramesets[0].IsFrameLinkToFile = false;
```

### Ayrıca bakınız

* class [FramesetCollection](../../framesetcollection/)
* class [Frameset](../)
* ad alanı [Aspose.Words.Framesets](../../frameset/)
* toplantı [Aspose.Words](../../../)


