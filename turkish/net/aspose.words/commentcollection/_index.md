---
title: CommentCollection Class
linktitle: CommentCollection
articleTitle: CommentCollection
second_title: .NET için Aspose.Words
description: Projelerinizde belge düzenlemeyi ve işbirliğini geliştirmek için Yorum düğümlerine kolay erişim sağlayan Aspose.Words.CommentCollection sınıfını keşfedin.
type: docs
weight: 430
url: /tr/net/aspose.words/commentcollection/
---
## CommentCollection class

Bir koleksiyona yazılmış erişim sağlar[`Comment`](../comment/) düğümler.

Daha fazla bilgi edinmek için şu adresi ziyaret edin:[Yorumlarla Çalışma](https://docs.aspose.com/words/net/working-with-comments/) belgeleme makalesi.

```csharp
public class CommentCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | Birini alır[`Comment`](../comment/) verilen indekste. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Bu koleksiyondan ve belgeden tüm düğümleri kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğüm koleksiyonu üzerinde basit bir "foreach" tarzı yineleme sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Belirtilen dizinde koleksiyona bir düğüm ekler. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar. |

## Örnekler

Bir yorumun "tamamlandı" olarak nasıl işaretleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 // Bir hatayı belirtmek için bir yorum ekleyin.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // Yorumların varsayılan olarak "false" olarak ayarlanan bir "Tamamlandı" bayrağı vardır.
// Bir yorum belgede bir değişiklik yapmamızı öneriyorsa,
// değişikliği uygulayabiliriz ve daha sonra düzeltmeyi belirtmek için "Tamamlandı" bayrağını da ayarlayabiliriz.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// "Yapıldı" olan yorumlar kendilerini farklılaştıracak
// soluk metin rengiyle "tamamlanmamış" olanlardan.
comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Add text to this paragraph.");
builder.CurrentParagraph.AppendChild(comment);

doc.Save(ArtifactsDir + "Comment.Done.docx");
```

### Ayrıca bakınız

* class [NodeCollection](../nodecollection/)
* ad alanı [Aspose.Words](../../aspose.words/)
* toplantı [Aspose.Words](../../)
