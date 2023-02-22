---
title: HtmlSaveOptions.ExportTocPageNumbers
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. HTML MHTML ve EPUB kaydedilirken içindekiler tablosuna sayfa numaralarının yazıp yazılmayacağını belirtir. Varsayılan değeryanlış .
type: docs
weight: 280
url: /tr/net/aspose.words.saving/htmlsaveoptions/exporttocpagenumbers/
---
## HtmlSaveOptions.ExportTocPageNumbers property

HTML, MHTML ve EPUB kaydedilirken içindekiler tablosuna sayfa numaralarının yazıp yazılmayacağını belirtir. Varsayılan değer`yanlış` .

```csharp
public bool ExportTocPageNumbers { get; set; }
```

### Örnekler

İçindekiler tablosu içeren bir belgeyi .html'ye kaydederken sayfa numaralarının nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

// Bir içindekiler tablosu ekleyin ve ardından belgeyi "Başlık" kullanılarak biçimlendirilmiş paragraflarla doldurun
// içindekiler tablosunun girdi olarak alacağı stil. Her giriş, solda başlık paragrafını görüntüler,
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
// TOC'mizin gösterdiği sayfa numaralarının hiçbir anlamı olmayacaktır.
// Belgeyi HTML'ye kaydettiğimizde, bu sayfa numaralarını TOC'den çıkarmak için bir SaveOptions nesnesi iletebiliriz.
// "ExportTocPageNumbers" bayrağını "true" olarak ayarlarsak,
// her TOC girişi, Microsoft Word'deki görünümünü koruyarak başlığı, ayırıcıyı ve sayfa numarasını görüntüler.
// "ExportTocPageNumbers" bayrağını "false" olarak ayarlarsak,
// kaydetme işlemi hem ayırıcıyı hem de sayfa numarasını atlayacak ve her giriş için başlığı olduğu gibi bırakacaktır.
HtmlSaveOptions options = new HtmlSaveOptions { ExportTocPageNumbers = exportTocPageNumbers };

doc.Save(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html", options);

string outDocContents = File.ReadAllText(ArtifactsDir + "HtmlSaveOptions.ExportTocPageNumbers.html");

if (exportTocPageNumbers)
{
    Assert.True(outDocContents.Contains(
        "<p style=\"margin-top:0pt; margin-bottom:0pt\">" +
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
        "<span>Entry 1</span>" +
        "</p>"));
}
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


