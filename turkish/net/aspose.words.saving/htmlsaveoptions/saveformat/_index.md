---
title: HtmlSaveOptions.SaveFormat
linktitle: SaveFormat
articleTitle: SaveFormat
second_title: .NET için Aspose.Words
description: Çok yönlü erişilebilirlik için Html, Mhtml, Epub, Azw3 veya Mobi formatlarındaki belgeleri kolayca kaydetmek için HtmlSaveOptions SaveFormat özelliğini keşfedin.
type: docs
weight: 460
url: /tr/net/aspose.words.saving/htmlsaveoptions/saveformat/
---
## HtmlSaveOptions.SaveFormat property

Bu kaydetme seçenekleri nesnesi kullanılırsa belgenin kaydedileceği biçimi belirtir. Html ,Mhtml ,Epub , Azw3 veyaMobi .

```csharp
public override SaveFormat SaveFormat { get; set; }
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

* enum [SaveFormat](../../../aspose.words/saveformat/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
