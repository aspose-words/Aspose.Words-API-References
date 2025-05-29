---
title: Section.ClearContent
linktitle: ClearContent
articleTitle: ClearContent
second_title: .NET için Aspose.Words
description: ClearContent yöntemiyle bölümleri zahmetsizce temizleyin. İş akışınızı geliştirin ve içerik yönetimi verimliliğinizi bugün artırın!
type: docs
weight: 110
url: /tr/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

Bölümü temizler.

```csharp
public void ClearContent()
```

## Notlar

Metnin metni[`Body`](../body/) temizlendiğinde, bölüm sonunu temsil eden yalnızca bir boş paragraf kalır.

Tüm üstbilgi ve altbilgilerin metni temizlenir, ancak[`HeaderFooter`](../../headerfooter/) nesnelerin kendileri kaldırılmaz.

## Örnekler

Bir bölümün içeriğinin nasıl temizleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// "ClearContent" metodunu çalıştırmak tüm bölüm içeriklerini kaldıracaktır
// ancak tekrar içerik eklemek için boş bir paragraf bırakın.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### Ayrıca bakınız

* class [Section](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
