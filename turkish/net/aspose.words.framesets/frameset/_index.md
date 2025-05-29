---
title: Frameset Class
linktitle: Frameset
articleTitle: Frameset
second_title: .NET için Aspose.Words
description: Belgelerde kusursuz çerçeve yönetimi için Aspose.Words.Framesets.Frameset sınıfını keşfedin. Web sayfalarınızı verimli çerçeve entegrasyonuyla geliştirin!
type: docs
weight: 3510
url: /tr/net/aspose.words.framesets/frameset/
---
## Frameset class

Bir çerçeve sayfasını veya çerçeveler sayfasındaki tek bir çerçeveyi temsil eder.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

```csharp
public class Frameset
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [Frameset](frameset/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [ChildFramesets](../../aspose.words.framesets/frameset/childframesets/) { get; } | Alt çerçevelerin ve çerçeve sayfalarının koleksiyonunu alır. |
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | Bu çerçevede görüntülenecek web sayfası URL'sini veya belge dosya adını alır veya ayarlar. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | içinde belirtilen web sayfası veya belge dosya adının geçerli olup olmadığını belirten bir değeri alır veya ayarlar.[`FrameDefaultUrl`](./framedefaulturl/) özellik, çerçevenin bağlı olduğu harici bir kaynaktır. |

## Notlar

Eğer[`ChildFramesets`](./childframesets/) özellik öğeler içeriyor, bu örnek bir çerçeve sayfasıdır, aksi takdirde tek bir çerçevedir.

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

* ad alanı [Aspose.Words.Framesets](../../aspose.words.framesets/)
* toplantı [Aspose.Words](../../)
