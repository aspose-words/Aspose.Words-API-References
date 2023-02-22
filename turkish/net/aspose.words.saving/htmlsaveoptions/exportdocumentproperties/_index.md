---
title: HtmlSaveOptions.ExportDocumentProperties
second_title: Aspose.Words for .NET API Referansı
description: HtmlSaveOptions mülk. Yerleşik ve özel belge özelliklerinin HTML MHTML veya EPUBa dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değeryanlış .
type: docs
weight: 130
url: /tr/net/aspose.words.saving/htmlsaveoptions/exportdocumentproperties/
---
## HtmlSaveOptions.ExportDocumentProperties property

Yerleşik ve özel belge özelliklerinin HTML, MHTML veya EPUB'a dışa aktarılıp aktarılmayacağını belirtir. Varsayılan değer`yanlış` .

```csharp
public bool ExportDocumentProperties { get; set; }
```

### Örnekler

Bir belgeyi .epub'a kaydederken belirli bir kodlamanın nasıl kullanılacağını gösterir.

```csharp
Document doc = new Document(MyDir + "Rendering.docx");

// Kaydeteceğimiz bir belgenin kodlamasını belirtmek için SaveOptions nesnesini kullanın.
HtmlSaveOptions saveOptions = new HtmlSaveOptions();
saveOptions.SaveFormat = SaveFormat.Epub;
saveOptions.Encoding = Encoding.UTF8;

// Varsayılan olarak, bir çıktı .epub belgesinin tüm içeriği tek bir HTML bölümünde olacaktır.
// Bölme kriteri, belgeyi birkaç HTML parçasına ayırmamızı sağlar.
// Belgeyi başlık paragraflarına bölmek için kriterleri belirleyeceğiz.
// Bu, belirli bir boyuttan daha önemli HTML dosyalarını okuyamayan okuyucular için kullanışlıdır.
saveOptions.DocumentSplitCriteria = DocumentSplitCriteria.HeadingParagraph;

// Belge özelliklerini dışa aktarmak istediğimizi belirtin.
saveOptions.ExportDocumentProperties = true;

doc.Save(ArtifactsDir + "HtmlSaveOptions.Doc2EpubSaveOptions.epub", saveOptions);
```

### Ayrıca bakınız

* class [HtmlSaveOptions](../)
* ad alanı [Aspose.Words.Saving](../../htmlsaveoptions/)
* toplantı [Aspose.Words](../../../)


