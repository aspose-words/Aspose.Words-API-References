---
title: ParagraphFormat.StyleIdentifier
second_title: Aspose.Words for .NET API Referansı
description: ParagraphFormat mülk. Bu biçimlendirmeye uygulanan paragraf stilinin yerel ayardan bağımsız stil tanımlayıcısını alır veya ayarlar.
type: docs
weight: 350
url: /tr/net/aspose.words/paragraphformat/styleidentifier/
---
## ParagraphFormat.StyleIdentifier property

Bu biçimlendirmeye uygulanan paragraf stilinin yerel ayardan bağımsız stil tanımlayıcısını alır veya ayarlar.

```csharp
public StyleIdentifier StyleIdentifier { get; set; }
```

### Örnekler

Giriş olarak başlık stillerini kullanarak bir belgeye içindekiler tablosunun (TOC) nasıl ekleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Belgenin ilk sayfasına bir içindekiler tablosu ekleyin.
// Tabloyu, 1'den 3'e kadar düzeylerdeki başlıklara sahip paragrafları alacak şekilde yapılandırın.
// Ayrıca girişlerini bizi götürecek köprüler olacak şekilde ayarlayın
// Microsoft Word'de sol tıklandığında başlığın konumuna.
builder.InsertTableOfContents("\\o \"1-3\" \\h \\z \\u");
builder.InsertBreak(BreakType.PageBreak);

// Başlık stillerine sahip paragraflar ekleyerek içindekiler tablosunu doldurun.
// Seviyesi 1 ile 3 arasında olan bu tür başlıkların her biri tabloda bir giriş oluşturacaktır.
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

// İçindekiler tablosu, güncel bir sonucu göstermek için güncellenmesi gereken türden bir alandır.
doc.UpdateFields();
doc.Save(ArtifactsDir + "DocumentBuilder.InsertToc.docx");
```

### Ayrıca bakınız

* enum [StyleIdentifier](../../styleidentifier/)
* class [ParagraphFormat](../)
* ad alanı [Aspose.Words](../../paragraphformat/)
* toplantı [Aspose.Words](../../../)


