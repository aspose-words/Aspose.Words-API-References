---
title: DocumentBuilder.MoveToParagraph
linktitle: MoveToParagraph
articleTitle: MoveToParagraph
second_title: .NET için Aspose.Words
description: DocumentBuilder MoveToParagraph yöntemiyle belgenizde zahmetsizce gezinin ve bölümünüzdeki herhangi bir paragrafa hızlı imleç hareketi sağlayın.
type: docs
weight: 600
url: /tr/net/aspose.words/documentbuilder/movetoparagraph/
---
## DocumentBuilder.MoveToParagraph method

İmleci geçerli bölümdeki bir paragrafa taşır.

```csharp
public void MoveToParagraph(int paragraphIndex, int characterIndex)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| paragraphIndex | Int32 | Gitmek istediğiniz paragrafın dizini. |
| characterIndex | Int32 | Paragrafın içindeki karakterin dizini. Negatif bir değer, paragrafın sonundan itibaren bir konum belirtmenize olanak tanır. Paragrafın sonuna gitmek için -1 kullanın. |

## Notlar

Gezinme, geçerli bölümün geçerli hikayesi içinde gerçekleştirilir. Yani, imleci ilk bölümün birincil başlığına, taşıdıysanız,*paragraphIndex* o bölümün header içindeki paragrafın dizinini belirtti.

Ne zaman*paragraphIndex* 0'dan büyük veya ona eşitse, bölümün başlangıcından itibaren bir dizin belirtir ve 0 ilk paragraftır.*paragraphIndex* 0, 'den küçükse, bölümün sonundan itibaren bir indeks belirtmiştir; -1 son paragraftır.

## Örnekler

Bir inşaatçının imleç konumunun belirtilen bir paragrafa nasıl taşınacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Paragraphs.docx");
ParagraphCollection paragraphs = doc.FirstSection.Body.Paragraphs;

Assert.AreEqual(22, paragraphs.Count);

// Belgeyi düzenlemek için belge oluşturucuyu oluşturun. Oluşturucunun imleci,
// belge oluşturma yöntemlerini çağırdığımızda yeni düğümler ekleyeceği nokta burasıdır,
// şu anda belgenin başında yer almaktadır.
DocumentBuilder builder = new DocumentBuilder(doc);

Assert.AreEqual(0, paragraphs.IndexOf(builder.CurrentParagraph));

// İmleci farklı bir paragrafa taşımak, imleci o paragrafın önüne getirecektir.
builder.MoveToParagraph(2, 0);
// Eklediğimiz her yeni içerik o noktada eklenecektir.
builder.Writeln("This is a new third paragraph. ");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
