---
title: FootnoteType Enum
linktitle: FootnoteType
articleTitle: FootnoteType
second_title: .NET için Aspose.Words
description: Aspose.Words.FootnoteType enum'u keşfedin. Gelişmiş belge biçimlendirmesi ve netlik için dipnotlar ve sonnotlar arasında kolayca ayrım yapın.
type: docs
weight: 5020
url: /tr/net/aspose.words.notes/footnotetype/
---
## FootnoteType enumeration

Bunun dipnot mu yoksa son not mu olduğunu belirtir.

```csharp
public enum FootnoteType
```

### değerler

| İsim | Değer | Tanım |
| --- | --- | --- |
| Footnote | `0` | Nesne bir dipnottur. |
| Endnote | `1` | Nesne bir dipnottur. |

## Notlar

Hem dipnotlar hem de sonnotlar nesneler tarafından temsil edilirFootnote sınıfı. Kullanım[`FootnoteType`](../footnote/footnotetype/) Dipnotlar ile sonnotlar arasında ayrım yapmak.

## Örnekler

Bir metne dipnot ve sonnotla nasıl atıfta bulunulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir miktar metin ekleyin ve bunu varsayılan olarak IsAuto özelliğini "true" olarak ayarlayarak bir dipnotla işaretleyin,
// böylece gövde metninde görülen işaretleyici otomatik olarak "1" olarak numaralandırılacak,
// ve dipnot sayfanın en altında görünecektir.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Daha fazla metin ekleyin ve özel bir referans işaretiyle bir dipnotla işaretleyin,
// "2" rakamının yerine kullanılacak ve "IsAuto" değeri false olarak ayarlanacak.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Dipnotlar her zaman atıfta bulunulan metnin en altında görünür,
// bu sayfa sonu dipnotu etkilemeyecektir.
// Öte yandan, dipnotlar her zaman belgenin sonunda yer alır
// böylece bu sayfa sonu dipnotu bir sonraki sayfaya itecektir.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

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

* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)
