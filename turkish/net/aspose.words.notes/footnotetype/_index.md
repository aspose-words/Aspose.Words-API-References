---
title: Enum FootnoteType
second_title: Aspose.Words for .NET API Referansı
description: Aspose.Words.Notes.FootnoteType Sıralama. Bunun dipnot mu yoksa son not mu olduğunu belirtir.
type: docs
weight: 4300
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
| Endnote | `1` | Nesne bir son nottur. |

### Notlar

Hem dipnotlar hem de sonnotlar nesneler tarafından temsil edilir.Footnote sınıfı. Kullanmak[`FootnoteType`](../footnote/footnotetype/) dipnotları ile son notları ayırt etmek için.

### Örnekler

Dipnot ve son not içeren metne nasıl başvurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir miktar metin ekleyin ve IsAuto özelliği varsayılan olarak "true" olarak ayarlanmış şekilde bir dipnotla işaretleyin,
// böylece gövde metninde görülen işaretçi "1" olarak otomatik olarak numaralandırılacaktır,
// ve dipnot sayfanın altında görünecektir.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Daha fazla metin ekleyin ve bunu özel referans işaretli bir son notla işaretleyin,
// "2" sayısı yerine kullanılacak ve "IsAuto" değeri false olarak ayarlanacak.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Dipnotlar her zaman başvurulan metnin altında görünür,
// böylece bu sayfa sonu dipnotu etkilemeyecektir.
// Öte yandan son notlar her zaman belgenin sonundadır
// böylece bu sayfa sonu son notu bir sonraki sayfaya itecektir.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

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

* ad alanı [Aspose.Words.Notes](../../aspose.words.notes/)
* toplantı [Aspose.Words](../../)


