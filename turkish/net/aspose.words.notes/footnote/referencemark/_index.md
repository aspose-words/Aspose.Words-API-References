---
title: Footnote.ReferenceMark
linktitle: ReferenceMark
articleTitle: ReferenceMark
second_title: .NET için Aspose.Words
description: Dipnotlarınızı ReferenceMark özelliğiyle özelleştirin. Belgelerinizde açıklık ve düzen için benzersiz işaretçileri kolayca ayarlayın. Bugün okunabilirliği artırın!
type: docs
weight: 60
url: /tr/net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

Bu dipnot için kullanılacak özel referans işaretini alır/ayarlar. Varsayılan değer**boş dize** (Empty ), otomatik numaralı dipnotların kullanıldığı anlamına gelir.

```csharp
public string ReferenceMark { get; set; }
```

## Notlar

Bu özellik şu şekilde ayarlanırsa**boş dize** (Empty ) veya`hükümsüz` , Daha sonra[`IsAuto`](../isauto/) özellik otomatik olarak ayarlanacaktır`doğru` , başka bir şeye ayarlanmışsa[`IsAuto`](../isauto/) ayarlanacak`YANLIŞ` .

RTF formatı yalnızca 1 sembolü özel referans işareti olarak saklayabilir, bu nedenle dışa aktarma sırasında yalnızca ilk sembol yazılacak, diğerleri atılacaktır.

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

* class [Footnote](../)
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
