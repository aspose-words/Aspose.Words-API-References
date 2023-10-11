---
title: Section.Body
second_title: Aspose.Words for .NET API Referansı
description: Section mülk. Şunu döndürürBody bölümün alt düğümü.
type: docs
weight: 20
url: /tr/net/aspose.words/section/body/
---
## Section.Body property

Şunu döndürür:[`Body`](../../body/) bölümün alt düğümü.

```csharp
public Body Body { get; }
```

### Notlar

[`Body`](../../body/) bölümün ana metnini içerir.

İadeler`hükümsüz` eğer bölüm yoksa[`Body`](../../body/) çocukları arasındaki düğüm.

### Örnekler

Belgedeki tüm bölümlerdeki ana metni, bölümleri bırakarak temizler.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraftan oluşur.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve çocuğu olmayan bir belge düğümü elde ederiz.
doc.RemoveAllChildren();

// Bu belgede artık içerik ekleyebileceğimiz bileşik alt düğüm yok.
// Eğer onu düzenlemek istiyorsak, düğüm koleksiyonunu yeniden doldurmamız gerekecek.
// Öncelikle yeni bir bölüm oluşturun ve ardından bunu alt öğe olarak kök belge düğümüne ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bir bölümün tüm içeriğini içerecek ve görüntüleyecek bir gövdeye ihtiyacı vardır
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bu gövdenin çocuğu yok, dolayısıyla ona henüz çalıştırma ekleyemiyoruz.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // Bu gövdenin en az bir boş paragraf içerdiğinden emin olmak için "EnsureMinimum"u çağırın.
body.EnsureMinimum();

// Artık gövdeye çalıştırmalar ekleyebilir ve belgenin bunları görüntülemesini sağlayabiliriz.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Body](../../body/)
* class [Section](../)
* ad alanı [Aspose.Words](../../section/)
* toplantı [Aspose.Words](../../../)


