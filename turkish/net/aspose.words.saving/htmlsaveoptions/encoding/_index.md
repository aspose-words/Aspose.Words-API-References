---
title: HtmlSaveOptions.Encoding
linktitle: Encoding
articleTitle: Encoding
second_title: .NET için Aspose.Words
description: Sorunsuz HTML, MHTML ve EPUB dışa aktarımları için HtmlSaveOptions Kodlamasını keşfedin. En iyi uyumluluk ve performans için kodlamayı UTF-8 ile kolayca özelleştirin.
type: docs
weight: 100
url: /tr/net/aspose.words.saving/htmlsaveoptions/encoding/
---
## HtmlSaveOptions.Encoding property

HTML, MHTML veya EPUB'a aktarırken kullanılacak kodlamayı belirtir. Varsayılan değer`yeni UTF8Kodlama(yanlış)` (BOM olmadan UTF-8).

```csharp
public Encoding Encoding { get; set; }
```

## Örnekler

Bir belgeyi .epub olarak kaydederken belirli bir kodlamanın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Kaydedeceğimiz belgenin kodlamasını belirtmek için SaveOptions nesnesini kullanın.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Varsayılan olarak, bir çıktı .epub belgesinin tüm içeriği tek bir HTML parçasında olacaktır.
// Bölme kriteri, belgeyi birkaç HTML parçasına ayırmamızı sağlar.
// Belgeyi başlık paragraflarına bölme kriterini belirleyeceğiz.
// Bu, belirli bir boyuttan daha büyük HTML dosyalarını okuyamayan okuyucular için yararlıdır.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Belge özelliklerini dışa aktarmak istediğimizi belirtelim.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
