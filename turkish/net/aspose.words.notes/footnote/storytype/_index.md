---
title: Footnote.StoryType
second_title: Aspose.Words for .NET API Referansı
description: Footnote mülk. İadelerFootnotes veyaEndnotes .
type: docs
weight: 60
url: /tr/net/aspose.words.notes/footnote/storytype/
---
## Footnote.StoryType property

İadelerFootnotes veyaEndnotes .

```csharp
public override StoryType StoryType { get; }
```

### Örnekler

InlineStory düğümlerinin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, null);

// Tablo düğümleri, tablonun en az bir hücreye sahip olmasını sağlayan bir "EnsureMinimum()" yöntemine sahiptir.
Table table = new Table(doc);
table.EnsureMinimum();

// Dipnotun içine, referans veren sayfanın altbilgisinde görünmesini sağlayacak bir tablo yerleştirebiliriz.
Assert.That(footnote.Tables, Is.Empty);
footnote.AppendChild(table);
Assert.AreEqual(1, footnote.Tables.Count);
Assert.AreEqual(NodeType.Table, footnote.LastChild.NodeType);

// Bir InlineStory'nin de bir "EnsureMinimum()" yöntemi vardır, ancak bu durumda,
// düğümün son çocuğunun bir paragraf olmasını sağlar,
// Microsoft Word'de kolayca tıklayıp metin yazabilmemiz için.
footnote.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, footnote.LastChild.NodeType);

// Küçük üst simge numarası olan bağlantının görünümünü düzenleyin
// ana metinde dipnota işaret eden.
footnote.Font.Name = "Arial";
footnote.Font.Color = Color.Green;

// Tüm satır içi hikaye düğümlerinin kendi hikaye türleri vardır.
Assert.AreEqual(StoryType.Footnotes, footnote.StoryType);

// Yorum satır içi hikayenin başka bir türüdür.
Comment comment = (Comment)builder.CurrentParagraph.AppendChild(new Comment(doc, "John Doe", "J. D.", DateTime.Now));

// Satır içi hikaye düğümünün ana paragrafı, ana belge gövdesindeki paragraf olacaktır.
Assert.AreEqual(doc.FirstSection.Body.FirstParagraph, comment.ParentParagraph);

// Ancak son paragraf yorum metni içeriğindeki paragraftır,
// bir konuşma balonunun içinde ana belge gövdesinin dışında olacak.
// Bir yorumda varsayılan olarak herhangi bir alt düğüm bulunmaz,
// böylece buraya da bir paragraf yerleştirmek için ProvidingMinimum() yöntemini uygulayabiliriz.
Assert.Null(comment.LastParagraph);
comment.EnsureMinimum();
Assert.AreEqual(NodeType.Paragraph, comment.LastChild.NodeType);

// Bir paragrafımız olduğunda, oluşturucuyu bunu yapması için hareket ettirebilir ve yorumumuzu yazabiliriz.
builder.MoveTo(comment.LastParagraph);
builder.Write("My comment.");

Assert.AreEqual(StoryType.Comments, comment.StoryType);

doc.Save(ArtifactsDir + "InlineStory.InsertInlineStoryNodes.docx");
```

### Ayrıca bakınız

* enum [StoryType](../../../aspose.words/storytype/)
* class [Footnote](../)
* ad alanı [Aspose.Words.Notes](../../footnote/)
* toplantı [Aspose.Words](../../../)


