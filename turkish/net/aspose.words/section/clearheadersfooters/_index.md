---
title: Section.ClearHeadersFooters
linktitle: ClearHeadersFooters
articleTitle: ClearHeadersFooters
second_title: .NET için Aspose.Words
description: ClearHeadersFooters yöntemiyle bölüm başlıklarını ve altbilgilerini zahmetsizce temizleyin. Cilalı bir görünüm için belge düzeninizi kolaylaştırın!
type: docs
weight: 120
url: /tr/net/aspose.words/section/clearheadersfooters/
---
## ClearHeadersFooters() {#clearheadersfooters}

Bu bölümün başlıklarını ve altbilgilerini temizler.

```csharp
public void ClearHeadersFooters()
```

## Notlar

Tüm üstbilgi ve altbilgilerin metni temizlenir, ancak[`HeaderFooter`](../../headerfooter/) nesnelerin kendileri kaldırılmaz.

Bu, bu bölümün üstbilgi ve altbilgilerinin önceki bölümün üstbilgi ve altbilgilerine bağlı olmasını sağlar.

## Örnekler

Bir bölümdeki tüm üstbilgi ve altbilgilerin içeriğinin nasıl temizleneceğini gösterir.

```csharp
Document doc = new Document();

Assert.AreEqual(0, doc.FirstSection.HeadersFooters.Count);

DocumentBuilder builder = new DocumentBuilder(doc);

builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Writeln("This is the primary header.");
builder.MoveToHeaderFooter(HeaderFooterType.FooterPrimary);
builder.Writeln("This is the primary footer.");

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual("This is the primary header.", doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("This is the primary footer.", doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Bu bölümdeki tüm üstbilgi ve altbilgilerin içeriklerini boşaltın.
// Başlıklar ve altbilgiler hala mevcut olacak ancak görüntülenecek hiçbir şey olmayacak.
doc.FirstSection.ClearHeadersFooters();

Assert.AreEqual(2, doc.FirstSection.HeadersFooters.Count);

Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual(string.Empty, doc.FirstSection.HeadersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
```

### Ayrıca bakınız

* class [Section](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## ClearHeadersFooters(*bool*) {#clearheadersfooters_1}

Bu bölümün başlıklarını ve altbilgilerini temizler.

```csharp
public void ClearHeadersFooters(bool preserveWatermarks)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| preserveWatermarks | Boolean | Filigranların kaldırılmaması gerekiyorsa doğrudur. |

## Notlar

Tüm üstbilgi ve altbilgilerin metni temizlenir, ancak[`HeaderFooter`](../../headerfooter/) nesnelerin kendileri kaldırılmaz.

Bu, bu bölümün üstbilgi ve altbilgilerinin önceki bölümün üstbilgi ve altbilgilerine bağlı olmasını sağlar.

## Örnekler

Başlık ve altbilgi içeriklerinin filigranlı veya filigransız nasıl temizleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Header and footer types.docx");

// Düz metin filigranı ekleyin.
doc.Watermark.SetText("Aspose Watermark");

// Başlık ve altbilgilerin içerik içerdiğinden emin olun.
HeaderFooterCollection headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("First header", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("Second header", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("Third header", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("First footer", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("Second footer", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("Third footer", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());

// Filigranlar hariç tüm üst bilgi ve alt bilgi içeriğini kaldırır.
doc.FirstSection.ClearHeadersFooters(true);

headersFooters = doc.FirstSection.HeadersFooters;
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.HeaderPrimary].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterFirst].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterEven].GetText().Trim());
Assert.AreEqual("", headersFooters[HeaderFooterType.FooterPrimary].GetText().Trim());
Assert.AreEqual(WatermarkType.Text, doc.Watermark.Type);

// Filigranlar dahil tüm başlık ve altbilgi içeriğini kaldırır.
doc.FirstSection.ClearHeadersFooters(false);
Assert.AreEqual(WatermarkType.None, doc.Watermark.Type);
```

### Ayrıca bakınız

* class [Section](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
