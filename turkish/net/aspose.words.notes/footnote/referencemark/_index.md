---
title: Footnote.ReferenceMark
linktitle: ReferenceMark
articleTitle: ReferenceMark
second_title: Aspose.Words for .NET
description: Footnote ReferenceMark mülk. Bu dipnot için kullanılacak özel referans işaretini alır/ayarlar. Varsayılan değerboş dize Empty  otomatik numaralandırılmış dipnotların kullanıldığı anlamına gelir C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.notes/footnote/referencemark/
---
## Footnote.ReferenceMark property

Bu dipnot için kullanılacak özel referans işaretini alır/ayarlar. Varsayılan değer:**boş dize** (Empty ), otomatik numaralandırılmış dipnotların kullanıldığı anlamına gelir.

```csharp
public string ReferenceMark { get; set; }
```

## Notlar

Bu özellik şu şekilde ayarlanırsa**boş dize** (Empty ) veya`hükümsüz` , Daha sonra[`IsAuto`](../isauto/) özellik otomatik olarak şu şekilde ayarlanacaktır:`doğru` , başka bir şeye ayarlanmışsa o zaman[`IsAuto`](../isauto/) şu şekilde ayarlanacak:`YANLIŞ` .

RTF-formatı özel referans işareti olarak yalnızca 1 sembolü saklayabilir, dolayısıyla dışa aktarma sırasında yalnızca ilk sembol yazılacak, diğerleri atılacaktır.

## Örnekler

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

* class [Footnote](../)
* ad alanı [Aspose.Words.Notes](../../../aspose.words.notes/)
* toplantı [Aspose.Words](../../../)
