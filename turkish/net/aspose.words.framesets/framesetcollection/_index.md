---
title: FramesetCollection Class
linktitle: FramesetCollection
articleTitle: FramesetCollection
second_title: .NET için Aspose.Words
description: Belge işlemede birden fazla Frameset örneğini zahmetsizce yönetmek için başvuracağınız çözüm olan Aspose.Words FramesetCollection sınıfını keşfedin.
type: docs
weight: 3520
url: /tr/net/aspose.words.framesets/framesetcollection/
---
## FramesetCollection class

Örneklerin bir koleksiyonunu temsil eder[`Frameset`](../frameset/) sınıf.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Belgelerle Programlama](https://docs.aspose.com/words/net/programming-with-documents/) belgeleme makalesi.

```csharp
public class FramesetCollection : IEnumerable<Frameset>
```

## yapıcılar

| İsim | Tanım |
| --- | --- |
| [FramesetCollection](framesetcollection/)() | Default_Constructor |

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words.framesets/framesetcollection/count/) { get; } | Koleksiyonda bulunan çerçeve veya çerçeve sayfalarının sayısını alır. |
| [Item](../../aspose.words.framesets/framesetcollection/item/) { get; } | Belirtilen dizinde bir çerçeve veya çerçeveler sayfası alır. |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [GetEnumerator](../../aspose.words.framesets/framesetcollection/getenumerator/)() | Koleksiyonda yineleme yapan bir numaralandırıcı döndürür. |

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

* class [Frameset](../frameset/)
* ad alanı [Aspose.Words.Framesets](../../aspose.words.framesets/)
* toplantı [Aspose.Words](../../)
