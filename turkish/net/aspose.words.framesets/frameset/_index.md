---
title: Class Frameset
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Framesets.Frameset sınıf. Bir çerçeve sayfasını veya çerçeveler sayfasındaki tek bir çerçeveyi temsil eder.
type: docs
weight: 3080
url: /tr/net/aspose.words.framesets/frameset/
---
## Frameset class

Bir çerçeve sayfasını veya çerçeveler sayfasındaki tek bir çerçeveyi temsil eder.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) dokümantasyon makalesi.

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
| [FrameDefaultUrl](../../aspose.words.framesets/frameset/framedefaulturl/) { get; set; } | Bu çerçevede görüntülenecek web sayfası URL'sini veya belge dosyası adını alır veya ayarlar. |
| [IsFrameLinkToFile](../../aspose.words.framesets/frameset/isframelinktofile/) { get; set; } | Web sayfası veya belge dosya adının the 'de belirtilip belirtilmediğini belirten bir değer alır veya ayarlar.[`FrameDefaultUrl`](./framedefaulturl/) özellik, çerçevenin bağlı olduğu harici bir kaynaktır. |

### Notlar

Eğer[`ChildFramesets`](./childframesets/) özelliği öğeler içeriyor, bu örnek bir çerçeve sayfasıdır, aksi takdirde tek bir çerçevedir.

### Örnekler

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

* ad alanı [Aspose.Words.Framesets](../../aspose.words.framesets/)
* toplantı [Aspose.Words](../../)


