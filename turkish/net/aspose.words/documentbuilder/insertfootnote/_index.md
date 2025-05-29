---
title: DocumentBuilder.InsertFootnote
linktitle: InsertFootnote
articleTitle: InsertFootnote
second_title: .NET için Aspose.Words
description: DocumentBuilder InsertFootnote yöntemiyle belgelerinizi zahmetsizce geliştirin; daha fazla netlik ve profesyonellik için dipnotları veya son notları kolayca ekleyin.
type: docs
weight: 340
url: /tr/net/aspose.words/documentbuilder/insertfootnote/
---
## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string*) {#insertfootnote}

Belgeye dipnot veya sonnot ekler.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| footnoteType | FootnoteType | Dipnot mu yoksa sonnot mu ekleneceğini belirtir. |
| footnoteText | String | Dipnotun metnini belirtir. |

### Geri dönüş değeri

Yeni oluşturulan dipnot nesnesini döndürür.

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

### Ayrıca bakınız

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## InsertFootnote(*[FootnoteType](../../../aspose.words.notes/footnotetype/), string, string*) {#insertfootnote_1}

Belgeye dipnot veya sonnot ekler.

```csharp
public Footnote InsertFootnote(FootnoteType footnoteType, string footnoteText, string referenceMark)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| footnoteType | FootnoteType | Dipnot mu yoksa sonnot mu ekleneceğini belirtir. |
| footnoteText | String | Dipnotun metnini belirtir. |
| referenceMark | String | Dipnotun özel referans işaretini belirtir. |

### Geri dönüş değeri

Yeni oluşturulan dipnot nesnesini döndürür.

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

### Ayrıca bakınız

* class [Footnote](../../../aspose.words.notes/footnote/)
* enum [FootnoteType](../../../aspose.words.notes/footnotetype/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
