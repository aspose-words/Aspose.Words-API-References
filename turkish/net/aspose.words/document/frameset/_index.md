---
title: Document.Frameset
linktitle: Frameset
articleTitle: Frameset
second_title: .NET için Aspose.Words
description: Belgeler için Frameset özelliğini keşfedin. Çerçeveli sayfaların sorunsuz entegrasyonu için bir Frameset örneği edinin. Web deneyiminizi bugün geliştirin!
type: docs
weight: 170
url: /tr/net/aspose.words/document/frameset/
---
## Document.Frameset property

Bir`Frameset` örneğin bu belge bir çerçeve sayfasını temsil ediyorsa.

```csharp
public Frameset Frameset { get; }
```

## Notlar

Belge çerçevelenmemişse, özellik şu şekildedir:`hükümsüz` değer.

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

* class [Frameset](../../../aspose.words.framesets/frameset/)
* class [Document](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
