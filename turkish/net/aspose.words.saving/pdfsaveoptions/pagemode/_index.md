---
title: PdfSaveOptions.PageMode
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. PDF belgesinin PDF okuyucuda açıldığında nasıl görüntülenmesi gerektiğini belirtir.
type: docs
weight: 250
url: /tr/net/aspose.words.saving/pdfsaveoptions/pagemode/
---
## PdfSaveOptions.PageMode property

PDF belgesinin PDF okuyucuda açıldığında nasıl görüntülenmesi gerektiğini belirtir.

```csharp
public PdfPageMode PageMode { get; set; }
```

### Notlar

Varsayılan değer:UseOutlines .

### Örnekler

Bazı PDF okuyucularının bir çıktı belgesini açarken izleyeceği talimatların nasıl ayarlanacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);
builder.Writeln("Hello world!");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// PDF okuyucunun kayıtlı dosyayı açmasını sağlamak için "PageMode" özelliğini "PdfPageMode.FullScreen" olarak ayarlayın
// monitörün ekranını devralan ve hiçbir kontrolün görünmediği tam ekran modunda belge.
// PDF okuyucunun ayrı bir panel görüntülemesini sağlamak için "PageMode" özelliğini "PdfPageMode.UseThumbs" olarak ayarlayın
// belgedeki her sayfa için bir küçük resim ile.
// PDF okuyucunun ayrı bir panel görüntülemesini sağlamak için "PageMode" özelliğini "PdfPageMode.UseOC" olarak ayarlayın
// bu, belgede bulunan tüm katmanlarla çalışmamıza olanak tanır.
// PDF okuyucuyu almak için "PageMode" özelliğini "PdfPageMode.UseOutlines" olarak ayarlayın
// mümkünse taslağı da görüntülemek için.
// PDF okuyucunun yalnızca belgenin kendisini görüntülemesini sağlamak için "PageMode" özelliğini "PdfPageMode.UseNone" olarak ayarlayın.
// Ekler panelini görünür hale getirmek için "PageMode" özelliğini "PdfPageMode.UseAttachments" olarak ayarlayın.
options.PageMode = pageMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageMode.pdf", options);
```

PDF'ye dönüştürdüğümüz bir belgedeki üstbilgi/altbilgilerdeki yer işaretlerinin işlenmesini gösterir.

```csharp
Document doc = new Document(MyDir + "Bookmarks in headers and footers.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions saveOptions = new PdfSaveOptions();

// Çıktı PDF'sinde anahat gezinme bölmesini görüntülemek için "PageMode" özelliğini "PdfPageMode.UseOutlines" olarak ayarlayın.
saveOptions.PageMode = PdfPageMode.UseOutlines;

// Tümünü görüntülemek için "DefaultBookmarksOutlineLevel" özelliğini "1" olarak ayarlayın
// çıktı PDF'sindeki ana hatların ilk düzeyindeki yer imleri.
saveOptions.OutlineOptions.DefaultBookmarksOutlineLevel = 1;

// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.None" olarak ayarlayın
// üstbilgi/altbilgi içindeki yer imlerini dışa aktarma.
// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.First" olarak ayarlayın
// yalnızca ilk bölümün üstbilgi/altbilgilerindeki yer işaretlerini dışa aktarın.
// "HeaderFooterBookmarksExportMode" özelliğini "HeaderFooterBookmarksExportMode.All" olarak ayarlayarak
// tüm üstbilgilerde/altbilgilerde bulunan yer işaretlerini dışa aktarın.
saveOptions.HeaderFooterBookmarksExportMode = headerFooterBookmarksExportMode;

doc.Save(ArtifactsDir + "PdfSaveOptions.HeaderFooterBookmarksExportMode.pdf", saveOptions);
```

### Ayrıca bakınız

* enum [PdfPageMode](../../pdfpagemode/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


