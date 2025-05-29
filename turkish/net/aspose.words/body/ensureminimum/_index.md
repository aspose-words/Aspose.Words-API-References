---
title: Body.EnsureMinimum
linktitle: EnsureMinimum
articleTitle: EnsureMinimum
second_title: .NET için Aspose.Words
description: İçeriğinizi Body EnsureMinimum yöntemiyle optimize edin. Daha iyi biçimlendirme için son çocuk paragraf değilse otomatik olarak boş bir paragraf ekleyin.
type: docs
weight: 70
url: /tr/net/aspose.words/body/ensureminimum/
---
## Body.EnsureMinimum method

Son çocuk bir paragraf değilse, boş bir paragraf oluşturur ve ekler.

```csharp
public void EnsureMinimum()
```

## Örnekler

Belgenin tüm bölümlerindeki ana metni temizler, bölümlerin kendisini bırakır.

```csharp
Document doc = new Document();

// Boş bir belge bir bölüm, bir gövde ve bir paragraftan oluşur.
// Tüm bu düğümleri kaldırmak için "RemoveAllChildren" yöntemini çağırın,
// ve çocuğu olmayan bir belge düğümüyle sonuçlanır.
doc.RemoveAllChildren();

// Bu belgenin artık içerik ekleyebileceğimiz bileşik alt düğümleri yok.
// Düzenlemek istersek, düğüm koleksiyonunu yeniden doldurmamız gerekecektir.
// İlk önce yeni bir bölüm oluşturun ve ardından onu kök belge düğümüne bir alt bölüm olarak ekleyin.
Section section = new Section(doc);
doc.AppendChild(section);

// Bir bölümün, tüm içeriklerini barındıracak ve görüntüleyecek bir gövdeye ihtiyacı vardır
// bölümün üstbilgisi ve altbilgisi arasındaki sayfada.
Body body = new Body(doc);
section.AppendChild(body);

// Bu gövdenin çocuğu yok, bu yüzden henüz ona koşu ekleyemiyoruz.
Assert.AreEqual(0, doc.FirstSection.Body.GetChildNodes(NodeType.Any, true).Count);

 // Bu gövdenin en az bir boş paragraf içerdiğinden emin olmak için "EnsureMinimum"u çağırın.
body.EnsureMinimum();

// Şimdi gövdeye çalıştırmalar ekleyebilir ve bunları görüntüleyecek belgeyi alabiliriz.
body.FirstParagraph.AppendChild(new Run(doc, "Hello world!"));

Assert.AreEqual("Hello world!", doc.GetText().Trim());
```

### Ayrıca bakınız

* class [Body](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
