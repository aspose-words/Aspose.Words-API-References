---
title: PdfSaveOptions.ExportParagraphGraphicsToArtifact
linktitle: ExportParagraphGraphicsToArtifact
articleTitle: ExportParagraphGraphicsToArtifact
second_title: .NET için Aspose.Words
description: Belgenizin görsel netliğini artırmak için paragraf grafiklerini eserler olarak kontrol etmek üzere PdfSaveOptions ExportParagraphGraphicsToArtifact özelliğini keşfedin.
type: docs
weight: 160
url: /tr/net/aspose.words.saving/pdfsaveoptions/exportparagraphgraphicstoartifact/
---
## PdfSaveOptions.ExportParagraphGraphicsToArtifact property

Bir paragraf grafiğinin bir yapıt olarak işaretlenip işaretlenmeyeceğini belirleyen bir değeri alır veya ayarlar.

```csharp
public bool ExportParagraphGraphicsToArtifact { get; set; }
```

## Notlar

Varsayılan değer`YANLIŞ` ve paragraf grafikleri (alt çizgiler, metin vurguları, vb.) belgenin mantıksal yapısında "Span" olarak işaretlenecektir.

Değer ne zaman`doğru` Paragraf grafikleri "Eser" olarak işaretlenecektir.

Bu değer şu durumlarda göz ardı edilir:[`ExportDocumentStructure`](../exportdocumentstructure/) dır`YANLIŞ` .

## Örnekler

Paragraf grafiklerinin eser olarak (alt çizgiler, metin vurguları, vb.) nasıl dışarı aktarılacağını gösterir.

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
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
