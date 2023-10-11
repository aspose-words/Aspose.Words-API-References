---
title: Footnote.Footnote
second_title: Aspose.Words for .NET API Referansı
description: Footnote inşaatçı. Bir örneğini başlatırFootnote class.
type: docs
weight: 10
url: /tr/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

Bir örneğini başlatır[`Footnote`](../) class.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahibi belgesi. |
| footnoteType | FootnoteType | A[`FootnoteType`](../footnotetype/) value bunun dipnot mu yoksa son not mu olduğunu belirtir. |

### Notlar

Ne zaman[`Footnote`](../) oluşturulduysa, belirtilen belgeye aittir ancak henüz değildir ve belgenin bir parçası değildir ve[`ParentNode`](../../../aspose.words/node/parentnode/) dır-dir`hükümsüz`.

Eklemek[`Footnote`](../) belge kullanımınaNode) veyaNode) Dipnotun eklenmesini istediğiniz paragrafta .

### Örnekler

Dipnotların nasıl ekleneceğini ve özelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metin ekleyin ve ona bir dipnotla referans verin. Bu dipnotta küçük bir üst simge referansı yer alacaktır
// başvuruda bulunduğu metnin sonrasını işaretleyin ve sayfanın altındaki ana gövde metninin altında bir giriş oluşturun.
// Bu giriş dipnotun referans işaretini ve referans metnini içerecektir,
// bunu belge oluşturucunun "InsertFootnote" yöntemine aktaracağız.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Bu özellik "true" olarak ayarlanırsa dipnotumuzun referans işareti
// bölümün tüm dipnotları arasında dizini olacaktır.
// Bu ilk dipnot olduğundan referans işareti "1" olacaktır.
Assert.True(footnote.IsAuto);

 // Referans metnini düzenlemek için belge oluşturucuyu dipnotun içine taşıyabiliriz.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Dipnotun indeks numarası yerine kullanacağı özel bir referans işareti ayarlayabiliriz.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// "IsAuto" bayrağı true olarak ayarlanmış bir yer imi yine de gerçek dizinini gösterecektir
// önceki yer imleri özel referans işaretlerini görüntülese bile, bu yer iminin referans işareti "3" olacaktır.
builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

Assert.True(footnote.IsAuto);

doc.Save(ArtifactsDir + "InlineStory.AddFootnote.docx");
```

### Ayrıca bakınız

* class [DocumentBase](../../../aspose.words/documentbase/)
* enum [FootnoteType](../../footnotetype/)
* class [Footnote](../)
* ad alanı [Aspose.Words.Notes](../../footnote/)
* toplantı [Aspose.Words](../../../)


