---
title: Footnote
linktitle: Footnote
articleTitle: Footnote
second_title: .NET için Aspose.Words
description: Dipnot Oluşturucumuzla zahmetsizce ilgi çekici dipnotlar oluşturun. İçeriğinizin netliğini ve profesyonelliğini sadece birkaç tıklamayla artırın!
type: docs
weight: 10
url: /tr/net/aspose.words.notes/footnote/footnote/
---
## Footnote constructor

Bir örneğini başlatır[`Footnote`](../) sınıf.

```csharp
public Footnote(DocumentBase doc, FootnoteType footnoteType)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | DocumentBase | Sahip belgesi. |
| footnoteType | FootnoteType | A[`FootnoteType`](../footnotetype/) Bunun dipnot mu yoksa sonnot mu olduğunu belirten value_x000d. |

## Notlar

Ne zaman[`Footnote`](../) oluşturulduğunda, belirtilen belgeye aittir, ancak henüz belgenin bir parçası değildir ve[`ParentNode`](../../../aspose.words/node/parentnode/) dır`hükümsüz`.

Eklemek için[`Footnote`](../) belge kullanımına[`InsertAfter`](../../../aspose.words/compositenode/insertafter/) veya[`InsertBefore`](../../../aspose.words/compositenode/insertbefore/) Dipnotun eklenmesini istediğiniz paragrafın üzerine yazın.

## Örnekler

Dipnotların nasıl ekleneceğini ve özelleştirileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Metin ekleyin ve bir dipnotla referans verin. Bu dipnot, küçük bir üst simge referansı yerleştirecektir
// referans verdiği metnin sonrasını işaretle ve sayfanın alt kısmındaki ana gövde metninin altında bir giriş oluştur.
// Bu giriş dipnotun referans işaretini ve referans metnini içerecektir.
// bunu belge oluşturucunun "InsertFootnote" metoduna geçireceğiz.
builder.Write("Main body text.");
Footnote footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Bu özellik "true" olarak ayarlanırsa, dipnotumuzun referans işareti
// bölümün tüm dipnotları arasında dizini olacaktır.
// Bu ilk dipnot olduğu için referans işareti "1" olacaktır.
Assert.True(footnote.IsAuto);

 // Belge oluşturucuyu dipnotun içine taşıyarak referans metnini düzenleyebiliriz.
builder.MoveTo(footnote.FirstParagraph);
builder.Write(" More text added by a DocumentBuilder.");
builder.MoveToDocumentEnd();

Assert.AreEqual("\u0002 Footnote text. More text added by a DocumentBuilder.", footnote.GetText().Trim());

builder.Write(" More main body text.");
footnote = builder.InsertFootnote(FootnoteType.Footnote, "Footnote text.");

// Dipnotun indeks numarası yerine kullanacağı özel bir referans işareti belirleyebiliriz.
footnote.ReferenceMark = "RefMark";

Assert.False(footnote.IsAuto);

// "IsAuto" bayrağı true olarak ayarlanmış bir yer imi hala gerçek dizinini gösterecektir
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
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
