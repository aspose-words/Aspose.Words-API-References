---
title: HtmlSaveOptions.ExportTocPageNumbers
linktitle: ExportTocPageNumbers
articleTitle: ExportTocPageNumbers
second_title: .NET için Aspose.Words
description: HtmlSaveOptions ile HTML, MHTML ve EPUB dışa aktarımlarında TOC sayfa numaralarını kontrol edin. Gezinmeyi ve kullanıcı deneyimini zahmetsizce geliştirin!
type: docs
weight: 270
url: /tr/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

HTML, MHTML ve EPUB kaydedilirken içerik tablosuna sayfa numaralarının yazılıp yazılmayacağını belirtir. Varsayılan değer`YANLIŞ` .

```csharp
public bool ExportTocPageNumbers { get; set; }
```

## Örnekler

İçindekiler tablosu olan bir belgeyi .html olarak kaydederken sayfa numaralarının nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// İçindekiler tablosunu ekleyin ve ardından belgeyi "Başlık" kullanılarak biçimlendirilmiş paragraflarla doldurun
// içerik tablosunun girişler olarak alacağı stil. Her giriş, soldaki başlık paragrafını görüntüler,
// ve sağdaki başlığı içeren sayfa numarası.
FieldToc fieldToc = (FieldToc)builder.InsertField(FieldType.FieldTOC, true);

builder.ParagraphFormat.Style = builder.Document.Styles["Heading 1"];
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 1");
builder.Writeln("Entry 2");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 3");
builder.InsertBreak(BreakType.PageBreak);
builder.Writeln("Entry 4");
fieldToc.UpdatePageNumbers();
doc.UpdateFields();

// HTML belgelerinin sayfaları yoktur. Bu belgeyi HTML'ye kaydedersek,
// İçindekiler tablomuzda gösterilen sayfa numaralarının hiçbir anlamı olmayacaktır.
// Belgeyi HTML'e kaydettiğimizde, bu sayfa numaralarını İçindekiler tablosundan çıkarmak için bir SaveOptions nesnesi geçirebiliriz.
// "ExportTocPageNumbers" bayrağını "true" olarak ayarlarsak,
// Her İçindekiler girişi, Microsoft Word'deki görünümünü koruyarak başlığı, ayırıcıyı ve sayfa numarasını görüntüler.
// "ExportTocPageNumbers" bayrağını "false" olarak ayarlarsak,
// kaydetme işlemi hem ayırıcıyı hem de sayfa numarasını atlayacak ve her girişin başlığını olduğu gibi bırakacaktır.
HtmlSaveOptions options = new HtmlSaveOptions { ExportTocPageNumbers = exportTocPageNumbers };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    Assert.True(outDocContents.Contains(
        "<span>Entry 1</span>" +
        "<span style=\"width:428.14pt; font-family:'Lucida Console'; font-size:10pt; display:inline-block; -aw-font-family:'Times New Roman'; " +
        "-aw-tabstop-align:right; -aw-tabstop-leader:dots; -aw-tabstop-pos:469.8pt\">.......................................................................</span>" +
        "<span>2</span>" +
        "</p>"));
}
else
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
        "<span>Entry 2</span>" +
        "</p>"));
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
