---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: Aspose.Words for .NET
description: DocumentBuilder InsertFootnote yöntem. Belgeye dipnot veya son not ekler C#'da.
type: docs
weight: 330
url: /tr/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string*) {#insertfootnote}

Belgeye dipnot veya son not ekler.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| footnoteType | FootnoteType | Dipnot mu yoksa son not mu ekleneceği belirlenir. |
| footnoteText | String | Dipnotun metnini belirtir. |

### Geri dönüş değeri

Yeni oluşturulan bir dipnot nesnesini döndürür.

## Örnekler

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

### Ayrıca bakınız

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string, string*) {#insertfootnote_1}

Belgeye dipnot veya son not ekler.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| footnoteType | FootnoteType | Dipnot mu yoksa son not mu ekleneceği belirlenir. |
| footnoteText | String | Dipnotun metnini belirtir. |
| referenceMark | String | Dipnotun özel referans işaretini belirtir. |

### Geri dönüş değeri

Yeni oluşturulan bir dipnot nesnesini döndürür.

## Örnekler

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

### Ayrıca bakınız

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
