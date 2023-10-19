---
title: PdfSaveOptions.CreateNoteHyperlinks
linktitle: CreateNoteHyperlinks
articleTitle: CreateNoteHyperlinks
second_title: Aspose.Words for .NET
description: PdfSaveOptions CreateNoteHyperlinks mülk. Ana metin öyküsündeki dipnot/sonnot referanslarının etkin köprülere dönüştürülüp dönüştürülmeyeceğini belirtir. Köprü tıklandığında ilgili dipnot/sonnota yönlendirir. VarsayılanYANLIŞ  C#'da.
type: docs
weight: 50
url: /tr/net/aspose.words.saving/pdfsaveoptions/createnotehyperlinks/
---
## PdfSaveOptions.CreateNoteHyperlinks property

Ana metin öyküsündeki dipnot/sonnot referanslarının etkin köprülere dönüştürülüp dönüştürülmeyeceğini belirtir. Köprü tıklandığında ilgili dipnot/sonnota yönlendirir. Varsayılan:`YANLIŞ` .

```csharp
public bool CreateNoteHyperlinks { get; set; }
```

## Örnekler

Dipnotların ve son notların köprü işlevi görmesini nasıl sağlayacağınızı gösterir.

```csharp
Document doc = new Document(MyDir + "Footnotes and endnotes.docx");

// Belgenin "Save" yöntemine aktarabileceğimiz bir "PdfSaveOptions" nesnesi oluşturun
// bu yöntemin belgeyi .PDF'ye dönüştürme biçimini değiştirmek için.
PdfSaveOptions options = new PdfSaveOptions();

// Tüm dipnot/sonnot sembollerini dönüştürmek için "CreateNoteHyperlinks" özelliğini "true" olarak ayarlayın
// metinde, tıklandığında bizi ilgili dipnotlara/son notlara götüren bağlantılar görevi görür.
// Dipnot/sonnot sembollerinin herhangi bir şeye bağlanmaması için "CreateNoteHyperlinks" özelliğini "false" olarak ayarlayın.
options.CreateNoteHyperlinks = createNoteHyperlinks;

doc.Save(ArtifactsDir + "PdfSaveOptions.NoteHyperlinks.pdf", options);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
