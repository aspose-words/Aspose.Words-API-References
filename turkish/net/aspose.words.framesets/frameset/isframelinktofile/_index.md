---
title: Frameset.IsFrameLinkToFile
linktitle: IsFrameLinkToFile
articleTitle: IsFrameLinkToFile
second_title: Aspose.Words for .NET
description: Frameset IsFrameLinkToFile mülk. Web sayfası veya belge dosya adının the de belirtilip belirtilmediğini belirten bir değer alır veya ayarlar.FrameDefaultUrl özellik çerçevenin bağlı olduğu harici bir kaynaktır C#'da.
type: docs
weight: 40
url: /tr/net/aspose.words.framesets/frameset/isframelinktofile/
---
## Frameset.IsFrameLinkToFile property

Web sayfası veya belge dosya adının the 'de belirtilip belirtilmediğini belirten bir değer alır veya ayarlar.[`FrameDefaultUrl`](../framedefaulturl/) özellik, çerçevenin bağlı olduğu harici bir kaynaktır.

```csharp
public bool IsFrameLinkToFile { get; set; }
```

## Örnekler

Sayfadaki çerçevelere nasıl erişileceğini gösterir.

```csharp
// Belge, diğer belgelere bağlantılar içeren birkaç çerçeve içerir.
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

* class [Frameset](../)
* ad alanı [Aspose.Words.Framesets](../../../aspose.words.framesets/)
* toplantı [Aspose.Words](../../../)
