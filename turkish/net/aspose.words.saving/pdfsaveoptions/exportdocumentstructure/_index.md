---
title: PdfSaveOptions.ExportDocumentStructure
linktitle: ExportDocumentStructure
articleTitle: ExportDocumentStructure
second_title: .NET için Aspose.Words
description: PdfSaveOptions ile belgenizin dışa aktarma yapısını kontrol edin. En iyi PDF çıktısı için ayarları kolayca yönetin ve iş akışı verimliliğinizi artırın.
type: docs
weight: 140
url: /tr/net/aspose.words.saving/pdfsaveoptions/exportdocumentstructure/
---
## PdfSaveOptions.ExportDocumentStructure property

Belge yapısının dışa aktarılıp aktarılmayacağını belirleyen bir değer alır veya ayarlar.

```csharp
public bool ExportDocumentStructure { get; set; }
```

## Notlar

Bu değer, PDF/A-1a, PDF/A-2a ve PDF/UA-1'e kaydederken göz ardı edilir çünkü bu uyumluluk için belge yapısı gereklidir.

Belge yapısının dışa aktarılmasının, özellikle büyük belgeler için bellek tüketimini önemli ölçüde artırdığını unutmayın.

## Örnekler

Belge yapı öğelerinin nasıl korunacağını gösterir, bu da belgemizi programlı olarak yorumlamamıza yardımcı olabilir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();
// Belge yapısının (etiketler gibi) "ExportDocumentStructure" özelliğini "true" olarak ayarlayın.
// Adobe Acrobat'ın "İçerik" gezinme bölmesi, dosya boyutunun artması pahasına.
// Belge yapısını dışa aktarmamak için "ExportDocumentStructure" özelliğini "false" olarak ayarlayın.
options.ExportDocumentStructure = exportDocumentStructure;

// Bu belgeyi kaydederken belge yapısını dışa aktardığımızı varsayalım. Bu durumda,
// Adobe Acrobat kullanarak açabilir ve başlık gibi öğeler için etiketler bulabiliriz
// ve bir sonraki paragrafa "Görünüm" -> "Göster/Gizle" -> "Gezinti bölmeleri" -> "Etiketler" yoluyla ulaşabilirsiniz.
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
