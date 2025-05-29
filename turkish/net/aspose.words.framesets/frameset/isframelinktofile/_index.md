---
title: Frameset.IsFrameLinkToFile
linktitle: IsFrameLinkToFile
articleTitle: IsFrameLinkToFile
second_title: .NET için Aspose.Words
description: Frameset IsFrameLinkToFile özelliğinin harici kaynakları sorunsuz bir şekilde bağlayarak web tasarımınızı nasıl geliştirdiğini keşfedin. Daha iyi performans için çerçevelerinizi optimize edin!
type: docs
weight: 40
url: /tr/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

içinde belirtilen web sayfası veya belge dosya adının geçerli olup olmadığını belirten bir değeri alır veya ayarlar.[`FrameDefaultUrl`](../framedefaulturl/) özellik, çerçevenin bağlı olduğu harici bir kaynaktır.

```csharp
public bool IsFrameLinkToFile { get; set; }
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

* class [Frameset](../)
* ad alanı [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* toplantı [Aspose.Words](../../../)
