---
title: InlineStory.FirstParagraph
second_title: Aspose.Words for .NET API Referansı
description: InlineStory mülk. Öyküdeki ilk paragrafı alır.
type: docs
weight: 10
url: /tr/net/aspose.words/inlinestory/firstparagraph/
---
## InlineStory.FirstParagraph property

Öyküdeki ilk paragrafı alır.

```csharp
public Paragraph FirstParagraph { get; }
```

### Örnekler

Bir paragrafa nasıl yorum ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Write("Hello world!");

Comment comment = new Comment(doc, "John Doe", "JD", DateTime.Today);
builder.CurrentParagraph.AppendChild(comment);
builder.MoveTo(comment.AppendChild(new Paragraph(doc)));
builder.Write("Comment text.");

Assert.AreEqual(DateTime.Today, comment.DateTime);

// Microsoft Word'de, düzenlemek veya yanıtlamak için belge gövdesindeki bu yorumu sağ tıklatabiliriz. 
doc.Save(ArtifactsDir + "InlineStory.AddComment.docx");
```

Dipnotların nasıl ekleneceğini ve özelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metin ekleyin ve bir dipnotla referans verin. Bu dipnot küçük bir üst simge referansı yerleştirecektir
// referans verdiği metinden sonra işaretleyin ve sayfanın altındaki ana gövde metninin altında bir giriş oluşturun.
// Bu giriş, dipnotun referans işaretini ve referans metnini içerecektir,
// belge oluşturucunun "InsertFootnote" yöntemine geçeceğiz.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Bu özellik "true" olarak ayarlanırsa dipnotumuzun referans işareti
// tüm bölümün dipnotları arasında indeksi olacaktır.
// Bu ilk dipnottur, dolayısıyla referans işareti "1" olacaktır.
Assert.True(footnote.IsAuto);

// Referans metnini düzenlemek için belge oluşturucuyu dipnotun içine taşıyabiliriz. 
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Dipnotun indeks numarası yerine kullanacağı özel bir referans işareti belirleyebiliriz.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// "IsAuto" bayrağı true olarak ayarlanmış bir yer imi gerçek dizinini göstermeye devam edecek
// önceki yer imleri özel referans işaretleri gösterse bile, bu nedenle bu yer iminin referans işareti "3" olacaktır.
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Ayrıca bakınız

* class [Paragraph](../../paragraph/)
* class [InlineStory](../)
* ad alanı [Aspose.Words](../../inlinestory/)
* toplantı [Aspose.Words](../../../)


