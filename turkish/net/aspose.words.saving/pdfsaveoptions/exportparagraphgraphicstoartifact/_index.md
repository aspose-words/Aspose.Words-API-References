---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
second_title: Aspose.Words for .NET API Referansı
description: PdfSaveOptions mülk. Bir paragraf grafiğinin yapıt olarak işaretlenip işaretlenmeyeceğini belirleyen bir değer alır veya ayarlar.
type: docs
weight: 160
url: /tr/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Bir paragraf grafiğinin yapıt olarak işaretlenip işaretlenmeyeceğini belirleyen bir değer alır veya ayarlar.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

### Notlar

Varsayılan değer:`YANLIŞ` ve paragraf grafikleri (alt çizgi, metin vurgusu vb.) belgenin mantıksal yapısında "Span" olarak işaretlenecektir.

Değer ne zaman`doğru` paragraf grafikleri "Yapı" olarak işaretlenecektir.

Bu değer şu durumlarda göz ardı edilir:[`ExportDocumentStructure`](../exportdocumentstructure/) dır-dir`YANLIŞ` .

### Örnekler

Paragraf grafiklerinin yapay olarak nasıl dışa aktarılacağını gösterir (alt çizgiler, metin vurgusu vb.).

```csharp
Document doc = new Document(MyDir + "PDF artifacts.docx");

PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.ExportDocumentStructure = true;
saveOptions.ExportParagraphGraphicsToArtifact = true;
saveOptions.TextCompression = PdfTextCompression.None;

doc.Save(ArtifactsDir + "PdfSaveOptions.ExportParagraphGraphicsToArtifact.pdf", saveOptions);
```

### Ayrıca bakınız

* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../pdfsaveoptions/)
* toplantı [Aspose.Words](../../../)


