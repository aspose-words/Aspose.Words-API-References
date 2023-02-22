---
title: Footnote.ReferenceMark
second_title: Aspose.Words for .NET API Referansı
description: Footnote mülk. Bu dipnot için kullanılacak özel referans işaretini alır/ayarlar. Varsayılan değer boş dize Empty  yani otomatik numaralandırılmış dipnotlar kullanılır.
type: docs
weight: 50
url: /tr/net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

Bu dipnot için kullanılacak özel referans işaretini alır/ayarlar. Varsayılan değer **boş dize** (Empty ), yani otomatik numaralandırılmış dipnotlar kullanılır.

```csharp
public string ReferenceMark { get; set; }
```

### Notlar

Bu özellik olarak ayarlanırsa **boş dize** (Empty ) veya boş, ardından[`IsAuto`](../isauto/) özellik otomatik olarak true olarak ayarlanır, başka bir şeye ayarlanırsa[`IsAuto`](../isauto/) false. olarak ayarlanacak

RTF formatı, özel referans işareti olarak yalnızca 1 sembolü saklayabilir, bu nedenle dışa aktarma sırasında yalnızca ilk sembol yazılacak, diğerleri silinecektir.

### Örnekler

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

* class [Footnote](../)
* ad alanı [Aspose.Words.Notes](../../footnote/)
* toplantı [Aspose.Words](../../../)


