---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: .NET için Aspose.Words
description: PDF'lerinizi PdfSaveOptions' CreateNoteHyperlinks ile geliştirin. Dipnotları ve son notları kolay gezinme için tıklanabilir bağlantılara dönüştürün. Varsayılan, false.
type: docs
weight: 60
url: /tr/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Ana metin öyküsündeki dipnot/sonnot referanslarının etkin köprü metinlerine dönüştürülüp dönüştürülmeyeceğini belirtir. Köprü metni tıklandığında ilgili dipnot/sonnot'a yönlendirilir. Varsayılan`YANLIŞ` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Örnekler

Dipnot ve sonnotların köprü metni işlevi görmesinin nasıl sağlanacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Belgenin "Kaydet" metoduna geçirebileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'e nasıl dönüştüreceğini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Tüm dipnot/sonnot sembollerini değiştirmek için "CreateNoteHyperlinks" özelliğini "true" olarak ayarlayın
// metinde yer alan bağlantılar, tıklandığında ilgili dipnot/sonnotlara götüren bağlantılar olarak işlev görür.
// Dipnot/sonnot sembollerinin herhangi bir şeye bağlanmaması için "CreateNoteHyperlinks" özelliğini "false" olarak ayarlayın.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
