---
title: PdfSaveOptions.ExportDocumentStructure
linktitle: ExportDocumentStructure
articleTitle: ExportDocumentStructure
second_title: Aspose.Words for .NET
description: PdfSaveOptions ExportDocumentStructure mülk. Belge yapısının dışa aktarılıp aktarılmayacağını belirleyen bir değer alır veya ayarlar C#'da.
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

Bu uyumluluk için belge yapısı gerekli olduğundan, PDF/A-1a, PDF/A-2a ve PDF/UA-1'e kaydederken bu değer göz ardı edilir.

Belge yapısını dışa aktarmanın, özellikle büyük belgeler için olmak üzere bellek tüketimini önemli ölçüde artırdığını unutmayın.

## Örnekler

Belgemizin programlı olarak yorumlanmasına yardımcı olabilecek belge yapısı öğelerinin nasıl korunacağını gösterir.

```csharp
Document doc = new Document();
DocumentBuilder builder = new DocumentBuilder(doc);

builder.ParagraphFormat.Style = doc.Styles["Heading 1"];
builder.Writeln("Hello world!");
builder.ParagraphFormat.Style = doc.Styles["Normal"];
builder.Write(
    "Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua.");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Belge yapısını, bu tür etiketleri, aracılığıyla kullanılabilir hale getirmek için "ExportDocumentStructure" özelliğini "true" olarak ayarlayın.
// Arttırılmış dosya boyutu karşılığında Adobe Acrobat'ın "İçerik" gezinme bölmesi.
// Belge yapısını dışa aktarmamak için "ExportDocumentStructure" özelliğini "false" olarak ayarlayın.
options.ExportDocumentStructure = exportDocumentStructure;

// Bu belgeyi kaydederken belge yapısını dışa aktardığımızı varsayalım. Bu durumda,
// Adobe Acrobat'ı kullanarak açabiliriz ve başlık gibi öğeler için etiketler bulabiliriz
// ve sonraki paragraf "Görüntüle" --> "Göster/Gizle" -> "Gezinme bölmeleri" --> "Etiketler".
doc.Save(ArtifactsDir + "PdfSaveOptions.ExportDocumentStructure.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
