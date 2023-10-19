---
title: HtmlSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: Aspose.Words for .NET
description: HtmlSaveOptions Encoding mülk. HTML MHTML veya EPUBa dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değeryeni UTF8Kodlamayanlış BOM olmadan UTF8 C#'da.
type: docs
weight: 100
url: /tr/net/aspose.words.saving/htmlsaveoptions/encoding/
---
## HtmlSaveOptions.Encoding property

HTML, MHTML veya EPUB'a dışa aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer:`yeni UTF8Kodlama(yanlış)` (BOM olmadan UTF-8).

```csharp
public Encoding Encoding { get; set; }
```

## Örnekler

Bir belgeyi .epub'a kaydederken belirli bir kodlamanın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Kaydedeceğimiz belgenin kodlamasını belirtmek için SaveOptions nesnesini kullanın.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Varsayılan olarak, bir çıktı .epub belgesinin tüm içeriği tek bir HTML bölümünde bulunur.
// Bölme kriteri, belgeyi birkaç HTML parçasına ayırmamıza olanak tanır.
// Belgeyi başlık paragraflarına bölmek için kriterleri belirleyeceğiz.
// Bu, belirli bir boyuttan daha büyük HTML dosyalarını okuyamayan okuyucular için kullanışlıdır.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Belge özelliklerini dışa aktarmak istediğimizi belirtin.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
