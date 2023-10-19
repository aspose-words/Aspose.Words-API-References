---
title: Section.ClearContent
linktitle: ClearContent
articleTitle: ClearContent
second_title: Aspose.Words for .NET
description: Section ClearContent yöntem. Bölümü temizler C#'da.
type: docs
weight: 90
url: /tr/net/aspose.words/section/clearcontent/
---
## Section.ClearContent method

Bölümü temizler.

```csharp
public void ClearContent()
```

## Notlar

metni[`Body`](../body/) temizlendiğinde, bölüm sonunu temsil eden yalnızca bir boş paragraf kalır.

Tüm üstbilgi ve altbilgilerin metni temizlenir, ancak[`HeaderFooter`](../../headerfooter/) nesnelerin kendisi kaldırılmaz.

## Örnekler

Bir bölümün içeriğinin nasıl temizleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.Write("Hello world!");

Assert.AreEqual("Hello world!", doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);

// "ClearContent" yöntemini çalıştırmak tüm bölüm içeriğini kaldıracaktır
// ancak tekrar içerik eklemek için boş bir paragraf bırakın.
doc.FirstSection.ClearContent();

Assert.AreEqual(string.Empty, doc.GetText().Trim());
Assert.AreEqual(1, doc.FirstSection.Body.Paragraphs.Count);
```

### Ayrıca bakınız

* class [Section](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
