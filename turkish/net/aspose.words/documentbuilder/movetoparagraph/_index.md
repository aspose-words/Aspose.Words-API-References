---
title: DocumentBuilder.MoveToParagraph
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. İmleci geçerli bölümdeki bir paragrafa taşır.
type: docs
weight: 570
url: /tr/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

İmleci geçerli bölümdeki bir paragrafa taşır.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| paragraphIndex | Int32 | Taşınacak paragrafın dizini. |
| characterIndex | Int32 | Paragrafın içindeki karakterin dizini. Negatif bir değer, paragrafın sonundan itibaren bir konum belirtmenize olanak tanır. Paragrafın sonuna gitmek için -1'i kullanın. |

### Notlar

Gezinme, geçerli bölümün geçerli öyküsü içinde gerçekleştirilir. Yani, imleci ilk bölümün birincil başlığına, götürdüyseniz, ardından*paragraphIndex* bölümün başlık içindeki paragrafın dizinini belirtti.

Ne zaman*paragraphIndex* 0'dan büyük veya ona eşitse, 0'ın ilk paragraf olduğu bölümün başlangıcındaki dizinini belirtir. Ne zaman*paragraphIndex* 0, 'den küçükse, son paragraf -1 olmak üzere bölümün sonundan itibaren bir dizin belirtir.

### Örnekler

Oluşturucunun imleç konumunun belirli bir paragrafa nasıl taşınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Belgeyi düzenlemek için belge oluşturucu oluşturun. İnşaatçının imleci,
// belge oluşturma yöntemlerini çağırdığımızda yeni düğümlerin ekleneceği nokta,
// şu anda belgenin başındadır.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// İmleci farklı bir paragrafa taşıdığınızda, imleç o paragrafın önüne yerleştirilecektir.
builder.MoveToParagraph(2, 0);
// Eklediğimiz yeni içerik bu noktada eklenecektir.
builder.Writeln("This is a new third paragraph. ");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


