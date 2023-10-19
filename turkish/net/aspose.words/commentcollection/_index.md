---
title: CommentCollection Class
linktitle: CommentCollection
articleTitle: CommentCollection
second_title: Aspose.Words for .NET
description: Aspose.Words.CommentCollection sınıf. Bir koleksiyona yazılı erişim sağlarComment düğümler C#'da.
type: docs
weight: 240
url: /tr/net/aspose.words/commentcollection/
---
## CommentCollection class

Bir koleksiyona yazılı erişim sağlar[`Comment`](../comment/) düğümler.

Daha fazlasını öğrenmek için şu adresi ziyaret edin:[Yorumlarla Çalışmak](https://docs.aspose.com/words/net/working-with-comments/) dokümantasyon makalesi.

```csharp
public class CommentCollection : NodeCollection
```

## Özellikleri

| İsim | Tanım |
| --- | --- |
| [Count](../../aspose.words/nodecollection/count/) { get; } | Koleksiyondaki düğüm sayısını alır. |
| [Item](../../aspose.words/commentcollection/item/) { get; } | Bir öğeyi alır[`Comment`](../comment/) verilen dizinde. (2 indexers) |

## yöntemler

| İsim | Tanım |
| --- | --- |
| [Add](../../aspose.words/nodecollection/add/)(*[Node](../node/)*) | Koleksiyonun sonuna bir düğüm ekler. |
| [Clear](../../aspose.words/nodecollection/clear/)() | Tüm düğümleri bu koleksiyondan ve belgeden kaldırır. |
| [Contains](../../aspose.words/nodecollection/contains/)(*[Node](../node/)*) | Bir düğümün koleksiyonda olup olmadığını belirler. |
| [GetEnumerator](../../aspose.words/nodecollection/getenumerator/)() | Düğümlerin koleksiyonu üzerinde basit bir "foreach" stili yinelemesi sağlar. |
| [IndexOf](../../aspose.words/nodecollection/indexof/)(*[Node](../node/)*) | Belirtilen düğümün sıfır tabanlı dizinini döndürür. |
| [Insert](../../aspose.words/nodecollection/insert/)(*int, [Node](../node/)*) | Belirtilen dizindeki koleksiyona bir düğüm ekler. |
| [Remove](../../aspose.words/nodecollection/remove/)(*[Node](../node/)*) | Düğümü koleksiyondan ve belgeden kaldırır. |
| [RemoveAt](../../aspose.words/nodecollection/removeat/)(*int*) | Belirtilen dizindeki düğümü koleksiyondan ve belgeden kaldırır. |
| [ToArray](../../aspose.words/nodecollection/toarray/)() | Koleksiyondaki tüm düğümleri yeni bir düğüm dizisine kopyalar. |

## Örnekler

Bir yorumun nasıl "tamamlandı" olarak işaretleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Helo world!");

 // Bir hatayı belirtmek için bir yorum ekleyin.
Comment comment = new Comment(doc, "John Doe", "J.D.", DateTime.Now);
comment.SetText("Fix the spelling error!");
doc.FirstSection.Body.FirstParagraph.AppendChild(comment);

 // Yorumlarda varsayılan olarak "yanlış" olarak ayarlanmış bir "Bitti" bayrağı bulunur.
// Bir yorum belge içinde değişiklik yapmamızı öneriyorsa,
// değişikliği uygulayabilir ve ardından düzeltmeyi belirtmek için "Bitti" bayrağını da ayarlayabiliriz.
Assert.False(comment.Done);

doc.FirstSection.Body.FirstParagraph.Runs[0].Text = "Hello world!";
comment.Done = true;

// "Tamamlanan" yorumlar kendilerini farklılaştıracaktır
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
