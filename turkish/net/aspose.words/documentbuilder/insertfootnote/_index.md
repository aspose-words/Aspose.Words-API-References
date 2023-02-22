---
title: DocumentBuilder.InsertFootnote
second_title: Aspose.Words for .NET API Referansı
description: DocumentBuilder yöntem. Belgeye bir dipnot veya son not ekler.
type: docs
weight: 310
url: /tr/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(FootnoteType, string) {#insertfootnote}

Belgeye bir dipnot veya son not ekler.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| footnoteType | FootnoteType | Dipnot mu yoksa son not mu ekleneceğini belirtir. |
| footnoteText | String | Dipnotun metnini belirtir. |

### Geri dönüş değeri

Yeni oluşturulmuş bir dipnot nesnesi döndürür.

### Örnekler

Dipnot ve son notla metne nasıl başvurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir metin ekleyin ve IsAuto özelliği varsayılan olarak "true" olarak ayarlanmış bir dipnotla işaretleyin,
// böylece gövde metninde görülen işaretçi otomatik olarak "1" olarak numaralandırılacaktır,
// ve dipnot sayfanın altında görünecektir.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Daha fazla metin ekleyin ve özel bir referans işareti içeren bir son notla işaretleyin,
// "2" yerine kullanılacak ve "IsAuto" değerini false olarak ayarlayacaktır.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Dipnotlar her zaman başvurulan metnin altında görünür,
// böylece bu sayfa sonu dipnotu etkilemeyecektir.
// Öte yandan, son notlar her zaman belgenin sonundadır
// böylece bu sayfa sonu son notu bir sonraki sayfaya itecektir.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Ayrıca bakınız

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)

---

## InsertFootnote(FootnoteType, string, string) {#insertfootnote_1}

Belgeye bir dipnot veya son not ekler.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| footnoteType | FootnoteType | Dipnot mu yoksa son not mu ekleneceğini belirtir. |
| footnoteText | String | Dipnotun metnini belirtir. |
| referenceMark | String | Dipnotun özel referans işaretini belirtir. |

### Geri dönüş değeri

Yeni oluşturulmuş bir dipnot nesnesi döndürür.

### Örnekler

Dipnot ve son notla metne nasıl başvurulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir metin ekleyin ve IsAuto özelliği varsayılan olarak "true" olarak ayarlanmış bir dipnotla işaretleyin,
// böylece gövde metninde görülen işaretçi otomatik olarak "1" olarak numaralandırılacaktır,
// ve dipnot sayfanın altında görünecektir.
builder.Write("This text will be referenced by a footnote.");
builder.InsertFootnote(FootnoteType.Footnote, "Footnote comment regarding referenced text.");

// Daha fazla metin ekleyin ve özel bir referans işareti içeren bir son notla işaretleyin,
// "2" yerine kullanılacak ve "IsAuto" değerini false olarak ayarlayacaktır.
builder.Write("This text will be referenced by an endnote.");
builder.InsertFootnote(FootnoteType.Endnote, "Endnote comment regarding referenced text.", "CustomMark");

// Dipnotlar her zaman başvurulan metnin altında görünür,
// böylece bu sayfa sonu dipnotu etkilemeyecektir.
// Öte yandan, son notlar her zaman belgenin sonundadır
// böylece bu sayfa sonu son notu bir sonraki sayfaya itecektir.
builder.InsertBreak(BreakType.PageBreak);

doc.Save(ArtifactsDir + "DocumentBuilder.InsertFootnote.docx");
```

### Ayrıca bakınız

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../documentbuilder/)
* toplantı [Aspose.Words](../../../)


