---
title: DocumentBuilder.MoveToParagraph
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. İmleci geçerli bölümdeki bir paragrafa taşır.
type: docs
weight: 540
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

Gezinme, geçerli bölümün geçerli öyküsü içinde gerçekleştirilir. Yani, imleci ilk bölümün birincil başlığına taşıdıysanız, o zaman paragrafIndex, o bölümün o header içindeki paragrafın dizinini belirtir.

paragrafIndex 0'dan büyük veya 0'a eşit olduğunda, ilk paragraf 0 olacak şekilde bölümün başlangıcından 'den bir dizin belirtir. paragrafIndex 0, 'den küçük olduğunda, son paragraf -1 olacak şekilde bölümün sonundan bir dizin belirledi.

### Örnekler

Oluşturucunun imleç konumunun belirtilen bir paragrafa nasıl taşınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Belgeyi düzenlemek için belge oluşturucu oluşturun. İnşaatçının imleci,
// belge oluşturma yöntemlerini çağırdığımızda yeni düğümler ekleyeceği nokta,
// şu anda belgenin başında.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// İmleci farklı bir paragrafa taşı, imleci o paragrafın önüne yerleştirir.
builder.MoveToParagraph(2, 0);
// Eklediğimiz her yeni içerik bu noktada eklenecektir.
builder.Writeln("This is a new third paragraph. ");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


