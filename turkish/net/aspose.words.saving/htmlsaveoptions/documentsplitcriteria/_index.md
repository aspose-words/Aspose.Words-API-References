---
title: HtmlSaveOptions.DocumentSplitCriteria
linktitle: DocumentSplitCriteria
articleTitle: DocumentSplitCriteria
second_title: .NET için Aspose.Words
description: HTML, EPUB ve AZW3 formatlarında belge kaydetmeyi optimize etmek için HtmlSaveOptions DocumentSplitCriteria özelliğini keşfedin. Biçimlendirme kontrolünüzü bugün geliştirin!
type: docs
weight: 80
url: /tr/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Belgenin kaydedilirken nasıl bölüneceğini belirtirHtml , Epub veyaAzw3 format. VarsayılanNone HTML ve içinHeadingParagraph EPUB ve AZW3 için.

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

## Notlar

Normalde bir belgeyi tek bir dosya olarak HTML'e kaydetmek istersiniz. Ancak bazı durumlarda çıktıyı birkaç küçük HTML sayfasına bölmek tercih edilebilir. HTML biçimine kaydedildiğinde bu sayfalar ayrı dosyalara veya akışlara çıktı olarak verilir. EPUB biçimine kaydedildiğinde ilgili paketlere dahil edilirler.

MHTML formatında kaydedilirken bir belge bölünemez.

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../../aspose.words.saving/)
* toplantı [Aspose.Words](../../../)
