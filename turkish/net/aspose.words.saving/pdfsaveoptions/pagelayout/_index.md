---
title: PdfSaveOptions.PageLayout
linktitle: PageLayout
articleTitle: PageLayout
second_title: .NET için Aspose.Words
description: PDF'nizin düzenini herhangi bir okuyucuda en iyi şekilde görüntülemek için özelleştirmek üzere PdfSaveOptions PageLayout özelliğini keşfedin. Belgenizin sunumunu geliştirin!
type: docs
weight: 250
url: /tr/net/aspose.words.saving/pdfsaveoptions/pagelayout/
---
## PdfSaveOptions.PageLayout property

Belge bir PDF okuyucusunda açıldığında kullanılacak sayfa düzenini belirtir.

```csharp
public PdfPageLayout PageLayout { get; set; }
```

## Notlar

Varsayılan değer:SinglePage .

## Örnekler

PDF okuyucusunda açıldığında sayfaların nasıl görüntüleneceğini gösterir.

```csharp
Document doc = new Document(MyDir + "Big document.docx");

// Sayfaları ikişer ikişer görüntüle, tek numaralı sayfalar solda olsun.
PdfSaveOptions saveOptions = new PdfSaveOptions();
saveOptions.PageLayout = PdfPageLayout.TwoPageLeft;

doc.Save(ArtifactsDir + "PdfSaveOptions.PageLayout.pdf", saveOptions);
```

### Ayrıca bakınız

* enum [PdfPageLayout](../../pdfpagelayout/)
* class [PdfSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
