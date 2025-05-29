---
title: InlineStory.LastParagraph
linktitle: LastParagraph
articleTitle: LastParagraph
second_title: .NET için Aspose.Words
description: Hikayenizin son paragrafına zahmetsizce erişmek ve içerik yönetimi deneyiminizi geliştirmek için InlineStory LastParagraph özelliğini keşfedin.
type: docs
weight: 70
url: /tr/net/aspose.words/inlinestory/lastparagraph/
---
## InlineStory.LastParagraph property

Hikayedeki son paragrafı alır.

```csharp
public Paragraph LastParagraph { get; }
```

## Örnekler

InlineStory düğümlerinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Tablo düğümlerinin, tablonun en az bir hücreye sahip olduğundan emin olan bir "EnsureMinimum()" yöntemi vardır.
Table table = new Table(doc);
table.EnsureMinimum();

// Dipnotun içine bir tablo yerleştirebiliriz, bu tablonun referans sayfasının alt bilgisinde görünmesini sağlar.
Assert.AreEqual(0, footnote.Tables.Count);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// Bir InlineStory'nin "EnsureMinimum()" yöntemi de vardır, ancak bu durumda,
// Düğümün son çocuğunun bir paragraf olduğundan emin olur,
// Microsoft Word'de yazıları tıklayıp kolayca yazabilmemiz için.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Küçük üst simge numarası olan çapanın görünümünü düzenleyin
// Dipnotu işaret eden ana metinde.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Tüm satır içi hikaye düğümlerinin kendi hikaye tipleri vardır.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// Yorum, satır içi hikayenin başka bir türüdür.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Satır içi hikaye düğümünün üst paragrafı, ana belge gövdesindeki paragraf olacaktır.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Ancak son paragraf yorum metin içeriğindendir,
// ana belge gövdesinin dışında bir konuşma balonu içinde yer alacaktır.
// Bir yorumun varsayılan olarak herhangi bir alt düğümü olmayacaktır,
// böylece EnsureMinimum() metodunu kullanarak buraya da bir paragraf yerleştirebiliriz.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// Bir paragrafımız olduğunda, oluşturucuyu hareket ettirip yorumumuzu yazabiliriz.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Ayrıca bakınız

* class [Paragraph](../../paragraph/)
* class [InlineStory](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
