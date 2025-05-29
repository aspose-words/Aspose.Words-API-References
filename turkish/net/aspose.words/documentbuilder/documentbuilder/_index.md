---
title: DocumentBuilder
linktitle: DocumentBuilder
articleTitle: DocumentBuilder
second_title: .NET için Aspose.Words
description: DocumentBuilder ile zahmetsizce güçlü belgeler oluşturun. Bugün yeni bir örnek başlatın ve belge yönetiminizi kolaylaştırın!
type: docs
weight: 10
url: /tr/net/aspose.words/documentbuilder/documentbuilder/
---
## DocumentBuilder() {#constructor}

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public DocumentBuilder()
```

## Notlar

Yeni bir tane oluşturur[`DocumentBuilder`](../)nesneyi yeni bir nesneye bağlar ve onu yeni bir nesneye bağlar[`Document`](../../document/) nesne.

## Örnekler

DocumentBuilder kullanılarak biçimlendirilmiş metnin nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Yazı tipi biçimlendirmesini belirtin, ardından metni ekleyin.
Aspose.Words.Font font = builder.Font;
font.Size = 16;
font.Bold = true;
font.Color = Color.Blue;
font.Name = "Courier New";
font.Underline = Underline.Dash;

builder.Write("Hello world!");
```

### Ayrıca bakınız

* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## DocumentBuilder(*[DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_3}

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public DocumentBuilder(DocumentBuilderOptions options)
```

## Notlar

Yeni bir tane oluşturur[`DocumentBuilder`](../)nesneyi yeni bir nesneye bağlar ve onu yeni bir nesneye bağlar[`Document`](../../document/) nesne. Ek belge oluşturma seçenekleri belirtilebilir.

## Örnekler

İçerik için tablo biçimlendirmesinin nasıl göz ardı edileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Tablodan önce içerik ekler.
// Varsayılan yazı tipi boyutu 12'dir.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Tablo içindeki yazı tipi boyutunu değiştirir.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// ContextTableFormatting true ise, tablo biçimlendirmesi içeriğe uygulanmaz.
// ContextTableFormatting false ise tablo biçimlendirmesi içeriğe sonradan uygulanır.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Ayrıca bakınız

* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/)*) {#constructor_1}

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public DocumentBuilder(Document doc)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | Document | The[`Document`](../../document/) bağlanacak nesne. |

## Notlar

Yeni bir tane oluşturur[`DocumentBuilder`](../) nesne, belirtilene bağlanır[`Document`](../../document/) nesne. İmleç belgenin başında konumlandırılmıştır.

## Örnekler

DocumentBuilder kullanılarak bir belgede üstbilgi ve altbilgilerin nasıl oluşturulacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İlk, çift ve tek sayfalar için farklı üstbilgi ve altbilgi istediğimizi belirtin.
builder.PageSetup.DifferentFirstPageHeaderFooter = true;
builder.PageSetup.OddAndEvenPagesHeaderFooter = true;

// Başlıkları oluşturun, ardından her başlık türünü görüntülemek için belgeye üç sayfa ekleyin.
builder.MoveToHeaderFooter(HeaderFooterType.HeaderFirst);
builder.Write("Header for the first page");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderEven);
builder.Write("Header for even pages");
builder.MoveToHeaderFooter(HeaderFooterType.HeaderPrimary);
builder.Write("Header for all other pages");

builder.MoveToSection(0);
builder.Writeln("Page1");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Page3");

doc.Save(ArtifactsDir + "DocumentBuilder.HeadersAndFooters.docx");
```

Başlık stillerini girdi olarak kullanarak bir belgeye İçindekiler Tablosu'nun (TOC) nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgenin ilk sayfasına bir içerik tablosu ekleyin.
// Tabloyu 1 ila 3 düzey başlıklarına sahip paragrafları alacak şekilde yapılandırın.
// Ayrıca, girişlerini bizi götürecek köprü metinleri olarak ayarlayın
// Microsoft Word'de sol tıklandığında başlığın bulunduğu yere.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Başlık stilleri içeren paragraflar ekleyerek içindekiler tablosunu doldurun.
// 1 ile 3 arasında bir seviyeye sahip her başlık tabloda bir girdi oluşturacaktır.
builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 1.1");
builder.Writeln("Heading 1.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading1;
builder.Writeln("Heading 2");
builder.Writeln("Heading 3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.1");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading3;
builder.Writeln("Heading 3.1.1");
builder.Writeln("Heading 3.1.2");
builder.Writeln("Heading 3.1.3");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading4;
builder.Writeln("Heading 3.1.3.1");
builder.Writeln("Heading 3.1.3.2");

builder.ParagraphFormat.StyleIdentifier = StyleIdentifier.Heading2;
builder.Writeln("Heading 3.2");
builder.Writeln("Heading 3.3");

// İçindekiler tablosu, güncel bir sonuç göstermek için güncellenmesi gereken bir tür alandır.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Ayrıca bakınız

* class [Document](../../document/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)

---

## DocumentBuilder(*[Document](../../document/), [DocumentBuilderOptions](../../documentbuilderoptions/)*) {#constructor_2}

Bu sınıfın yeni bir örneğini başlatır.

```csharp
public DocumentBuilder(Document doc, DocumentBuilderOptions options)
```

| Parametre | Tip | Tanım |
| --- | --- | --- |
| doc | Document | The[`Document`](../../document/) bağlanacak nesne. |
| options | DocumentBuilderOptions | Belge oluşturma süreci için ek seçenekler. |

## Notlar

Yeni bir tane oluşturur[`DocumentBuilder`](../) nesne, belirtilene bağlanır[`Document`](../../document/) nesne. İmleç belgenin başında konumlandırılmıştır.

## Örnekler

İçerik için tablo biçimlendirmesinin nasıl göz ardı edileceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilderOptions builderOptions = new DocumentBuilderOptions();
builderOptions.ContextTableFormatting = true;
DocumentBuilder builder = new DocumentBuilder(doc, builderOptions);

// Tablodan önce içerik ekler.
// Varsayılan yazı tipi boyutu 12'dir.
builder.Writeln("Font size 12 here.");
builder.StartTable();
builder.InsertCell();
// Tablo içindeki yazı tipi boyutunu değiştirir.
builder.Font.Size = 5;
builder.Write("Font size 5 here");
builder.InsertCell();
builder.Write("Font size 5 here");
builder.EndRow();
builder.EndTable();

// ContextTableFormatting true ise, tablo biçimlendirmesi içeriğe uygulanmaz.
// ContextTableFormatting false ise tablo biçimlendirmesi içeriğe sonradan uygulanır.
builder.Writeln("Font size 12 here.");

doc.Save(ArtifactsDir + "Table.ContextTableFormatting.docx");
```

### Ayrıca bakınız

* class [Document](../../document/)
* class [DocumentBuilderOptions](../../documentbuilderoptions/)
* class [DocumentBuilder](../)
* ad alanı [Aspose.Words](../../../aspose.words/)
* toplantı [Aspose.Words](../../../)
