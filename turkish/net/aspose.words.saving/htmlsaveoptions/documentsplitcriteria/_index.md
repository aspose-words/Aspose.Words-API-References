---
title: HtmlSaveOptions.DocumentSplitCriteria
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Belgeyi kaydederken nasıl bölünmesi gerektiğini belirtirHtml  Epub veyaAzw3 biçim. VarsayılanNone HTML ve içinHeadingParagraph EPUB ve AZW3. için
type: docs
weight: 80
url: /tr/net/aspose.words.saving/htmlsaveoptions/documentsplitcriteria/
---
## HtmlSaveOptions.DocumentSplitCriteria property

Belgeyi kaydederken nasıl bölünmesi gerektiğini belirtirHtml , Epub veyaAzw3 biçim. Varsayılan:None HTML ve içinHeadingParagraph EPUB ve AZW3. için

```csharp
public DocumentSplitCriteria DocumentSplitCriteria { get; set; }
```

### Notlar

Normalde bir belgenin HTML'ye tek bir dosya olarak kaydedilmesini istersiniz. Ancak bazı durumlarda çıktının birkaç küçük HTML sayfasına bölünmesi tercih edilir. HTML formatında kaydederken bu sayfalar ayrı dosyalara veya akışlara aktarılacaktır. EPUB formatında kaydederken ilgili paketlere dahil edileceklerdir.

MHTML formatında kaydederken bir belge bölünemez.

### Örnekler

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

* enum [DocumentSplitCriteria](../../documentsplitcriteria/)
* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


